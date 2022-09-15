In order to start developing solutions in Python, we will need to modularize some parts of the code in order to use it in the different solutions. Here are some of the pros and cons of using libraries in python:

Pros:
- You only have one base of truth, that means that when you have to do modifications or bug fixing you will only have to do it in one place.
- You won't need to publish a Serverless or API solution for this generic block of code if you want it to be independent.
- As a different repository and development stages, it won't be binded to the monorepo stages.
- Using Azure Devops Artifact functionality we will have control of the versioning and publishing of the code.
- Library security by having it in a private package manager.

Cons:
- We will be exposing all the functionality of the library, but because it is an internal library it won't generate great issues.
- Versioning releasing in Artifacts platform can sometimes be complex.
- Testing libraries in your code can sometimes be complicated.