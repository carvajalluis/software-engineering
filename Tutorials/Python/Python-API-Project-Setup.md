# Prerequisites

## Windows

### Install Virtualenv

Open a Terminal as an Administrator

Run
- pip install virtualenv


# Project Setup

## Open a Terminal in the branch you want the project

## Create a new folder for the project, for example: templateApi

mkdir templateApi

## Move to the new folder

cd templateApi

## Create a virtual Environment.

### Windows

virtualenv venv

## Create AWS Policy

On AWS Console go to IAM.

On the left panel click on Policies.

On the right panel at the top click the button "Create policy".

Click on JSON tab.

Copy the following text.

`{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "logs:CreateLogStream",
                "ssm:GetParameters",
                "logs:CreateLogGroup",
                "logs:PutLogEvents",
                "ssm:GetParameter"
            ],
            "Resource": [
                "arn:aws:logs:*:423165890424:log-group:/ECSLogs*",
                "arn:aws:ssm:*:423165890424:parameter/qa/service/*"
            ]
        }
    ]
}`

On the bottom click "Next: Tags"
On the bottom click "Next: Review"
Type the Policy name as follows:
The ServiceName specified in the file: azure-pipelilne-ecs.yaml located in the root of the current project; followed by a hyphen, the word 'service', followed by a hyphen, and the environment you are using.
For example:

- campaignapi-service-qa

And click Create Policy.

## Create the Role
On the left panel click Roles.

On the right panel at the top click "Create role"
On "Select type of trusted entiry" select "AWS service"
Select "Elastic Container Service" then at the bottom select "Elastic Container Service Task".
Click "Next: Permissions"
Select the policy you just created on the previous step.
Click "Next: Tags"
Click "Next: Review"
Type the Role name as follows:
The ServiceName specified in the file: azure-pipelilne-ecs.yaml located in the root of the current project; followed by a hyphen, the word 'service', followed by a hyphen, and the environment you are using.
Click "Create role"







