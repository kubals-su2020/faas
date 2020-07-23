# faas
Lambda function is written in nodejs and subscribes to sns topic:password_reset
Once it receives an event it triggers a dynamodb entry and also sends a mail to reset password on the first request in 15 minutes.