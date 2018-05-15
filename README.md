# turbodeploy
A simple serverless deployer for AWS Lambda

# Installation
1) Create an AWS Function with CloudFormation and CFTPL using the example in this repo (see caveats below)
2) Install this tool  `curl "https://raw.githubusercontent.com/my-ideas/turbodeploy/master/turbodeploy" -o ~/bin/turbodeploy; chmod +x ~/bin/turbodeploy`

# Usage
`turbodeploy update <env> [aws profile]`
Zip the current folder and upload a new version for this AWS Lambda function. 
* stage is then stage name
* profile is the AWS profile to use (if empty use credentials defined in ENVS)

`turbodeploy package`
Build npde dependencies using an Amazon Linux container 

# Caveats/configuration
Handler name must be `index.awslambda`


In the lambda repo, add a configuration file named `SERVERLESS`
```bash
MYI_FUNCTION_NAME=project-$stage-name
``` 

* MYI_FUNCTION_NAME := the name of the lamnbda function. You can use $STAGE to get the stage name

# Developing
Clone this repo and symlink it somewher in your $PATH.
`ln -s $PWD/turbodeploy ~/bin/turbodeploy`

