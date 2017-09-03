# Introduction

A very basic Cognito Cloudformation stack that will setup

- Cognito User Pool
- Cognito Identity Pool
- IAM Roles (authenticated - unauthenticated)
- IAM Role Policies

# Cloudformation commands

## Creating stacks

You can execute the stack from the command line like this: 

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
