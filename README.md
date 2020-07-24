# faas
Lambda function is written in nodejs and subscribes to sns topic:password_reset
Once it receives an event it triggers a dynamodb entry and also sends a mail to reset password on the first request in 15 minutes.

Environment varibales are as follows

DOMAIN NAME
SOURCE EMAIL ADDRESS

Usage
A CircleCI JOB will trigger a new deployment of lambda function
or following can also be used curl -u <circleci_user_token> -d build_parameters[CIRCLE_JOB]=build https://circleci.com/api/v1.1/project/github/<username>/faas/tree/master