SOLID applies to better principle for Object Oriented and Functional Programming:

* **S**ingle Responsibility Principle: 
  > The class should have one and only one reason to change
  Only do one thing was taken from imperative programming in the first place. Having small, focused functions is good.

* **O**pen Closed principle: 
  > Software entities should be open for extension but closed for modification.

  Allowing you to change behaviors without modifying code is good. Functional Programming uses higher-order functions more than inheritance, but the principle holds.

* **L**iskov Substitution Principle:
  > Objects in a program should be replaceable with instances of their subtypes without altering the correctness of that program

  Abiding by some interface contract is just as good in functional programming as in object-oriented. If a sort function takes a comparator, then you would expect the '0 is equals, less than provides negative results, greater than positive results' behavior.

* **I**nterface Segregation Principle: 
  > Keep interfaces small so that users don’t end up depending on things they don’t need.]
  
  Most functional languages still have structs. Specifying the smallest set of data required by a function is still good practice. Requiring the least specific interface to the data (why use Lists of ints when Enumerations of T work just as well?) is still good practice.

* **D**ependency Inversion Principle: 
  > Entities must depend on abstractions, not on concretions

  Specifying parameters to a function (or a higher-order function to retrieve them) rather than hard-coding the function to go get some value is just as good in functional programming as in object-oriented.

And even when doing object-oriented programming, many of these principles apply to the design of methods in the objects too.

### Reference:
  * https://medium.com/@mkocik/solid-principles-in-functional-programming-b9b83aeddf80
  * https://stackoverflow.com/questions/5577054/solid-for-functional-programming
  * https://towardsdatascience.com/solid-coding-in-python-1281392a6a94