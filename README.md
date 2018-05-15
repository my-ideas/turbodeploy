# turbodeploy
A simple serverless deployer for AWS Lambda

## Why not serverless
[Serverless](https://serverless.com/) is great but it has the following problems for us:
* Definition of the function: serverless requires the definition of the lambda to be with the code.
* CloudFormation stacks must have the stage in their name
* We must be able to package our nodejs function with dependencies compatible with the runtime environment.

# Developing
Clone this repo and symlink it somewher in your $PATH.
`ln -s $PWD/turbodeploy ~/bin/turbodeploy`

