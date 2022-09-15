These conventions look forward to keeping consistency between API and database  fields, classes and database naming

## MongoDB Database Naming

### Guidelines

- Use alphanumeric characters [a-z 0-9]
- Database names are case sensitive.
- Database names must have fewer than 64 characters.
- Database names for Windows operating system: 
  - Database names should contain alphanumeric characters.
  - Below special symbols are not allowed on Linux/Unix OS.
  ```
  Symbols not allowed in Database names : / \ . ” $  * < > : | ?
  ```
- Database names cannot be empty.
- Database names should not contain null or space characters or an empty string.
- Do not Use separators on a database name
### Example 

- `Account_Personal, Account-Personal, accountPersonal, Account Personal` :x:
- `AccountPersonal` :heavy_check_mark:

Note: You may like to extend the above pattern to add more fields like Org names or domain or subdomain names if following DDD (Domain-Driven Design) like org names etc.


`Microsoft_Account_Personal` :heavy_check_mark:


## MongoDB Collection Naming
### Guidelines
- Use Pascal Casing names. It is preferred to use a lower case to avoid any unwanted problems with casing.
- Collection names should not begin with below special characters like:
- Do not use separators on a collection name
### Example
- `account_record, Account_Record, account-record` :x:
- `AccountRecord` :heavy_check_mark:

Note: You can extend the above pattern to add more names like module or domain name etc.

## MongoDB Field Names Conventions
### Guidelines
- snake_case.
- Field names can not contain: 
  - null character
  - empty string
  - “.”
- Field names can not start with the dollar sign $ character
- Do not use separators on a field name

`name, city, account, lastName, accountNumber, AccountNumber` :x: 
`name, city, account, last_name, account_number` :heavy_check_mark:

Sample JSON example using snake_case field names,
```
{ 
  "_id" : "01001", 
  "name" : "TheCodeBuzz", 
  "last_name" : "TheCodeBuzz", 
  "city" : "newyork", 
  "state" : "NY",
  "account_name" :"TEST",
  "account_number":123
}
```