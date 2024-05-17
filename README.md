# AWS-Glue
Template repository for built in AWS Glue

## Directory Structure
`./src/cloudformation`  
Example CloudFormation template (CFT)

Substitute the template with placeholder values relevant to your application

`./src/config`  
Example environment configurations for deployments

Take special note to the columnMap, useful for transforming your data set during runtime

`./src/glue-job`  
Directory for the Glue job script.

Most integrations should generate their own Glue Jobs Code, but it is possible to generate multiple integrations sharing one GlueJob Code

`./src/sample-scripts`  
This folder contains a growing library of code snippets for connecting to various data sources

This should be removed from your project before deploy

`./AWS_application_deploy.sh`
This is a simple deployment script that can be used to deploy your application. If you are trying to have CI/CD functioning.

The script requires some setup before it can be used.  See the script source for more details

`./setup.cfg`
This is the configuration file for flake8, the python coding standard i'm are using for all glue jobs

I'm planning to enforce a flake8 quality gate in the future, in order for build and deployments to complete in GitActions
Make sure you set up a flake8 linter in your IDE, or run flake8 from command line regularly