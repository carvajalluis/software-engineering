# Metadata
Author: @<7A07745B-F1A5-402D-877E-083DE50303B1> 
Audience: Omneural Development Team

#Goals
The purpose of this assessment/audit is to encourage continued discussions on areas of improvements regarding  current state architecture. Additionally, the intent is to enable the sharing of information across the team regarding the design choices and tradeoffs. Note, this is just one engineers findings and perspective of the system.

#Background
The omneural system (formerly known as DAS) is used to build and execute dynamic marketing campaigns for small to mid-sized companies. Broadly defined, a marketing campaign is a cohesive and planned promotion of a product, service or concept in order to improve awareness or drive conversions for said product, service or concept. Marketing campaigns frequently showcase similar messaging across multiple channels (direct mail, SMS, digital ads, email, etc.) and push campaign members down conditional workflows which determine how and when a member is contacted. Omneural allows its users to accomplish this by combining Audiences and Workflows to schedule and execute Campaigns in an automated fashion through an easy-to-use User Interface.

# Summary
The omneural application has been undergoing both an application and architectural shift from a monolithic(c# application) to microservices(FastAPI/NextJS) state. The application is hosted on AWS and primarily utilizes serverless framework to run all its services.The application uses mongoDB cloud for datastore and Azure devops for remote repository and semi-automated deployment processes.


#Potential Areas of Improvement

##Completion of migration to microservices
Benefits:
- Standardize web frameworks (FastAPI/NextJS) and languages (Python)
- Deprecate legacy service - cost
- Enable faster build out of additional features (i.e. Azure SSO)
- maintainability + breaches
- shared libraries

Tradeoffs:
- Development commitment

##Identify and implement shared caching
Benefits:
- Decreased latency - DB/app processing
- DB read/queries
- State management - prevent duplicate jobs

Tradeoffs:
- Cost - implementation/hardware
- Complexity - in-cache data management

##Utilizing workflow services (i.e. AWS Step Functions) for complex workflows
Benefits:
- State management - restart jobs at failed state
- Simplified workflow

Tradeoffs:
- Implementation commitment
- Cost

##Shift from serverless to Fargate/ECS architecture for certain services and use cases
Notably there were quite a few number of lambdas with max level timeouts. For lambdas that deal with large datasets and complex logic it may be worth hosting it in a server.
Benefits:
- Processing scalability - no timeout
- generic serverless/server benefits and tradeoffs (i.e. deployment package size restrictions)
- Simplified architecture
- Easy lift and shift

Tradeoffs:
- less elastic cost

##E2E & Integration Tests
Benefits:
- Move towards a more CICD process.
- Less bugs and business logic ambiguity
- Higher development/deployment confidence

Tradeoffs:
- Significant investment in creating testing framework and architecture
- Developer adoption

##Persistence/durability
Currently app is heavily reliant on one region --> us-east-1. Design architecture to enable supporting other US regions. us-east-1 is one of the most heavily used regions
Benefits:
- region based outages likeliness decreases drastically

Tradeoffs:
- Cost
- Architecture and build out infra to sync regions

##Update ReadMe's - Service Info & local setup instructions
Benefits:
- Faster developer onboarding
- Prevent incorrect feature builds in each microservice

Tradeoffs:
- None

#Questions
* Usage of SNS/SQS. Very limited subscriptions on each SNS topic. FastAPI has async capabilities.
* Cleanup Jobs - outdates prospects
* Response recording flow

#Referencesid=%2Fsites%2FResearchandDevelopment%2FShared%20Documents%2FOmneural%20Application%2FTechnical%20Design%2FArchitecture%2FDAS%20%2D%20Technical%20Design%20Document%2Epdf&parent=%2Fsites%2FResearchandDevelopment%2FShared%20Documents%2FOmneural%20Application%2FTechnical%20Design%2FArchitecture)