## What triggers this workflow to run?

The workflow is triggered when code is pushed to main. This is shown on the on: section of the deploy.yml file. Every time a new commit is pushed to main, the Actions page automatically starts the workflow.

## What are the four main steps this workflow performs.

The four main steps are: 
    1. Checkout code
    2. Set up Node.js
    3. Install dependencies
    4. Deploy

## What does the "checkout code" step do and why is it necessary?

The Checkout Code stop downloads the repository's source code onto the Action runner. It gives the workflow access to the files it needs to build and deploy the action. It is necessary because Action starts as a clean environment, and doesn't automatically contain the source code. Without checking out the repository, the later steps wouldn't have the application files they need.

## What is the purpose of the environment configuration?

The environment configuration provide the settings and credentials that are needed for deployment in the workflow. The configuration also shows which environment is being deployed to providing information such as variables, deployment credentials, and other configurations

## How does this automated deployment improve reliability compared to manual deployment?

Automated deployment is able to perform the same steps every deployment in order to consistently improve reliability. It also is capable of removing human error, such as mistakes like forgetting a file or a step in the process. It is meant to save time by helping the developer to not deal with manually performing the deployment process after every change. Actions can automatically run deployment whenever a specified trigger occurs.

## What would happen if you pushed code to a different branch (not main)?

IF code were pushed onto a different branch than main, the workflow wouldn't run at all, as it is onl triggered when changes are made to main. Workflow doesn't trigger unless the changes are merged into main and a push to main triggers the workflow.