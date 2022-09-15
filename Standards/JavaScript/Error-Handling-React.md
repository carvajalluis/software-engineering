 ```js
  // childLoadError.js
  // define custom Error
  class ChildLoadError extends Error {
      constructor(...args) {
          super(...args)
          // hides parent constructor
          Error.captureStackTrace(this, ChildLoadError)
      }
  }
  ```

  ```js
  // childArrayMap.js
  port const childArrayMap = (childen) => {
    return childen.map((child) => {
      return {
        accountId: child.accountId,
        companyName: child.companyName,
        ownerEmail: child.ownerEmail
      }
    });
  }
  ```

  ```js
  // api.js
  export async function getChildAccounts() {
    try {
      const result = await xfetch(
        baseUrl + '/api/accounts/children',
        {
          method: 'GET'
        }
      );
      if (!result) {
        // maps empty result to empty array with atributes
        return childArrayMap([]);
      }
      const { childen } = await result.json();
      return childArrayMap(childStats);
    } catch (e) {
      let error = new ChildLoadError('Unable to load information');
      // custom property setting up a error code as a reference
      error.code = "E001"
      throw error
    }
  }
  ```

  ```js
  // Component.js
  useEffect(() => {
      const loadChildAccounts = async () => {
        const childAccounts = await getChildAccounts();
        let childAccounts = childArrayMap([]);
        try {
          childAccounts = await getChildAccounts();
        } catch (e) {
          onError(e);
        }
        setData({ childAccounts });
      };
      loadChildAccounts();
    }, []);
  ```


