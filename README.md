# Introduction

A very basic Cognito Cloudformation stack that will setup

- Cognito User Pool
- Cognito Identity Pool
- IAM Roles (authenticated - unauthenticated)
- IAM Role Policies

# Cloudformation commands

I'm going to export the stack name as the variable `STACK`

```
export STACK=cognito-stack
```

You can execute stack commands using the AWS CLI from the command line like this (make sure you're in the folder where the stack file resides.): 

## Creating stacks

```
aws cloudformation create-stack --capabilities CAPABILITY_NAMED_IAM --stack-name ${STACK} --template-body file://${STACK}.yml
```

## Updating a stack

```
aws cloudformation update-stack --stack-name ${STACK} --template-body file://${STACK}.yml 
```
## Deleting stack

```
aws cloudformation delete-stack --stack-name $STACK
```

## Getting stack info (you can also use console for this)

```
aws cloudformation describe-stack-events --stack-name $STACK | egrep "ResourceStatus|ResourceType"
```
