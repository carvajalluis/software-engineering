# Summary

Omneural microservices run on serverless framework on AWS infrastructure. Most of the API services (name: `<service>-api`) run on FastAPI and other core backend services similarly run on AWS lambda. The frontend framework omneural runs on is NextJS.

# Local provisioning Instructions

prerequisite:
1. clone [serverless repo](https://dev.azure.com/GoStrata/Omneural/_git/serverless)
2. Install PyCharm, venv, pyenv
3. Install python 3.9+
4. In PyCharm install Plugins: EnvFile (Borys), Pydantic (Koudai)

## API Services
1. Under serverless repo, open service in Pycharm
2. Pycharm will autoprompt creating Python Interpreter using pyenv. Create the interpreter.
3. You can also manage interpreter config by going to Preferences -> Project: <name> -> Python Interpreter.
4. Create .env file. [Env variable Library](https://dev.azure.com/GoStrata/Omneural/_library?itemType=VariableGroups)
5. In Pycharm IDE, click on Run/Edit Launch Configuration -> Edit Configuration -> module name: uvicorn -> Parameters: `main:app --reload --port <portNum>` -> Select appropriate Python Interpreter -> Select Env Tab and add created env file -> Click Apply and Save -> Click Run Button

## WebApp

1. Install yarn: `brew install yarn`
2. Verify on supported node version: `node --version`
3. Run development application: `yarn dev`

