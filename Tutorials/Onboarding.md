This wiki is intended to help with the onboarding when a new member joins the Omneural team

[[_TOC_]]


# Overview



# Product Description

# Technologies Stack

If you are the kind of person that like new challenges, this project is for you :). The DAS project has an interesting Technology Stack that is not very common to find but those technologies are the ones that make more sense for the Client's needs and will help them to scale down and up as needed.

- **Git** for source control
- Fast API python Rest API framework to develop all new microservices 
- React JS as front end Library to simplify client development
- MongoDB, a NO-SQL database management system, currently hosted on the mongo cloud 
- AWS Simple Queue Service (SQS)
- AWS Simple Notification Service (SNS)
- AWS Cloud Watch
- AWS Online Storage (S3)
- AWS Serverless Compute  (Lambda)
- Serverless Framework
  We understand that not all people are familiar with all those technologies or have worked with them a long time ago. This project represents a good **opportunity** to refresh your mind on those or get familiar with them. It is a good time to **refresh and strengthens your skills**.

## Training Curriculum

Below you will find some links we encourage you to visit and if you are the kind of person that likes new challenges, get a certification in any one of them (you could start with the easy one)

  - REACT
    * [React Tutorial](https://reactjs.org/tutorial/tutorial.html)
    * [reactjs docs/getting-started](https://reactjs.org/docs/getting-started.html)
    * [React Course](https://www.udemy.com/course/react-the-complete-guide-incl-redux/)
  - NEXT
      - [NextJS tutorial](https://nextjs.org/learn/basics/create-nextjs-app)
      - [NextJS docs/getting-started](https://nextjs.org/docs/getting-started)
  - API
    * [Rest API tutorial](https://restfulapi.net/)
    *   [HTTP statuses](https://httpstatuses.com/)
    *   [FastAPI](https://fastapi.tiangolo.com)
  - MONGODB
    * [Mongo Basics Learning Path](https://university.mongodb.com/learning_paths/developer)
  - [AWS Simple Queue Service (SQS)](https://aws.amazon.com/sqs/)
  - [AWS Simple Notification Service (SNS)](https://aws.amazon.com/sns)
  - [AWS CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/)

# Local Setup

The following links will redirect you to the official pages of each of the tools we used in the team. So you can download, install them and start playing.

- [Git](https://git-scm.com/downloads)
- [Fork](https://git-fork.com/) GUI tool for Git  
- [Visual Studio Code](https://code.visualstudio.com/download)
- [QueryAssist](https://queryassist.com) for mongo DB querying.
- [NodeJS](https://nodejs.org/en/download/) 
- [Yarn](https://classic.yarnpkg.com/en/docs/install/#windows-stable) for a node package manager that is efficient.
- [Postman](https://www.postman.com/downloads/) HTTP debugging and testing
- [Microsoft Teams](https://www.microsoft.com/en-us/microsoft-teams/download-app) mandatory communications app
- [PritUnl](https://client.pritunl.com/) for screenshot sharing or one of your preference
- [CyberDuck](https://cyberduck.io/download/) for SFTP and S3 access

# Team Workflow

Omneural Team is working under the Agile methodology and best practices. We have a two-week sprint. Also, before that day the team has another pre-demo meeting where we evaluate all the items the team could complete during the Sprint and which ones couldn't see what is going to be demoed the next day.

# Guide to good practices

There is plenty of good practices that were set up from the beginning of this project and others as the team goes on. We are trying to work as best as possible and these good practices will help you to streamline to workflow considerably.  they are to be found in this wiki.

## Code Reviews Standard and Checklist

We need to reinforce our culture of collaboration and learning in peer reviews.  Please review with all details the Standard as it is your best guide for conducting code reviews, and resolving conflicts and contains detailed steps of what to look for in a code review.

- [Pull Requests](https://dev.azure.com/strataResDev/DAS/_wiki/wikis/DAS.wiki/4/Source-Control-Management-Standard?anchor=pull-requests)

Please keep the following **steps/recommendations** as your main checklist when you are performing a **code review**:
What to look for in a code review
In doing a code review, you should make sure that:

- The code is well-designed.
- The functionality is good for the users of the code.
- Any UI changes are sensible and look good.
- Any parallel programming ( like multithreading, throw-away jobs, or using parallel computing libraries like Plinq, threads, asyncio) is done safely.
- The code isn’t more complex than it needs to be.
- The developer isn’t implementing things for the future that aren't  needed right now.
- The code has appropriate unit tests.
- Tests are well-designed.
- The developer used clear names for everything.
- Comments are clear, useful, and mostly explain why instead of what.
- The code is appropriately documented. [TODO: not clear yet documentation at the time of writing this document]
- The code conforms to our style guides.

# Architecture

We have some architecture diagrams that will help you understand the scope of this project as well as how it will connect to other services. You can find more information in the following [link](https://dev.azure.com/strataResDev/DAS/_wiki/wikis/DAS.wiki/22/Architecture) 