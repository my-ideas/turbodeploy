# turbodeploy
A simple serverless deployer for AWS Lambda

# Step By Step
1) Create an AWS Function with CloudFormation and CFTPL using the example in this repo (see caveats below)
2) 

# Caaveats/configuration
handler must be index.awslambda

## Why not serverless
[Serverless](https://serverless.com/) is great but it has the following problems for us:
* Definition of the function: serverless requires the definition of the lambda to be with the code.
* CloudFormation stacks must have the stage in their name
* We must be able to package our nodejs function with dependencies compatible with the runtime environment.

# Developing
Clone this repo and symlink it somewher in your $PATH.
`ln -s $PWD/turbodeploy ~/bin/turbodeploy`

