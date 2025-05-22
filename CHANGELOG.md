## 1.0.0 (2025-05-22)


### Bug Fixes

* Add configuration schema to plugin ([d51ac0c](https://github.com/davec-fvr/serverless-plugin-lambda-dead-letter/commit/d51ac0c84dff98930050b74c1558eb75633d6770))
* fixed validation and updated publish workflow ([1d4756f](https://github.com/davec-fvr/serverless-plugin-lambda-dead-letter/commit/1d4756f726e3a795ea05f45ca4ca133341e3d6dc))
* updated lifecycle hook for v3 required changes ([59618f5](https://github.com/davec-fvr/serverless-plugin-lambda-dead-letter/commit/59618f52b317e49570c543d6fc91cada5f76681d))

## 1.0.0 (2023-02-24)


### Bug Fixes

* Add configuration schema to plugin ([d51ac0c](https://github.com/digitalmaas/serverless-plugin-lambda-dead-letter/commit/d51ac0c84dff98930050b74c1558eb75633d6770))
* updated lifecycle hook for v3 required changes ([59618f5](https://github.com/digitalmaas/serverless-plugin-lambda-dead-letter/commit/59618f52b317e49570c543d6fc91cada5f76681d))

# 1.2.1 (2017-01-31)

## Bug Fixes
* Removed the plugin command `setLambdaDeadLetterConfig` because it didn't work in all scenarios.

## Meta
* [Comparison since last release](https://github.com/gmetzker/serverless-plugin-lambda-dead-letter/compare/v1.2.0...v1.2.1)


# 1.2.0 (2017-01-30)

## Features
* Dead Letter Queue properties #12

## Meta
* [Git Hub Mile Stone](https://github.com/gmetzker/serverless-plugin-lambda-dead-letter/milestone/2?closed=1)
* [Comparison since last release](https://github.com/gmetzker/serverless-plugin-lambda-dead-letter/compare/v1.1.0...v1.2.0)


# 1.1.0 (2017-01-29)

## Features
* Simplified syntax to create new SQS queue and use it in the function's `DeadLetterConfig.TargetArn` #10
* Simplified syntax to create a new SNS topic and use it in the function's `DeadLetterConfig.TargetArn` #11
* Validate function `deadLetter` object before deploy #26

 ## Bug Fixes
 * Do not call `UpdateFunctionConfiguration` when `--noDeploy` option is specified #19

 ## Meta
 * [Git Hub Mile Stone](https://github.com/gmetzker/serverless-plugin-lambda-dead-letter/milestone/3?closed=1)
 * [Comparison since last release](https://github.com/gmetzker/serverless-plugin-lambda-dead-letter/compare/v1.0.0...v1.1.0)

# 1.0.0 (2017-01-15)

## Features
* Basic support to assign the Lambda `DeadLetterConfig` using after serverless Cloudformation stack is deployed.  [Amazon Docs](http://docs.aws.amazon.com/lambda/latest/dg/dlq.html)
  * Plugin makes a call to the [Lambda Api](http://docs.aws.amazon.com/lambda/latest/dg/API_UpdateFunctionConfiguration.html)
 `UpdateFunctionConfiguration`
* Using a pre-existing SQS Queue or SNS Topic as a dead letter target.
* Using an SNS Queue or SNS Topic created in the resources section.
* Remove a previously existing dead letter `targetArn` by specifying a blank `targetArn`
