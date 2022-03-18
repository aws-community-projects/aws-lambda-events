---
description: List of general resources that could be used with all AWS Lambda by programming language
---

# General Resources

List of general resources that could be used with all AWS Lambda by language.

- [Python - AWS Lambda Powertools](https://awslabs.github.io/aws-lambda-powertools-python/latest/){target="_blank"}
- [Java - AWS Lambda Powertools](https://awslabs.github.io/aws-lambda-powertools-java/){target="_blank"}
- [Bref - Php](https://bref.sh/){target="_blank"} - php runtime and libraries
- [Go - AWS Lambda for Go](https://github.com/aws/aws-lambda-go){target="_blank"} - Event typing, Libraries, samples, and tools to help Go developers develop AWS Lambda functions. 
- [Typescript - AWS Lambda Powertools](https://awslabs.github.io/aws-lambda-powertools-typescript/latest/){target="_blank"}
- [Typescript - @types/aws-lambda](https://www.npmjs.com/package/@types/aws-lambda){target="_blank"} - NPM `@types/aws-lambda`
- [Rust - aws-lambda-rust-runtime](https://github.com/awslabs/aws-lambda-rust-runtime){target="_blank"} - runtime and framework and will soon include `aws_lambda_events` 
- [Rust - aws_lambda_events](https://github.com/LegNeato/aws-lambda-events){target="_blank"} - structs for most lambda events
- [Ruby - Jets](https://rubyonjets.com){target="_blank"} - Ruby Serverless Framework 

## Lambda Shareable test events

Create initial [Amazon EventBridge (CloudWatch Events) schema registry](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-schema-registry.html) for your Lambda functions.

```script
aws schemas create-registry --registry-name lambda-testevent-schemas --description "List of tests events for AWS Lambda" --tags comment=lambda-testevent-schemas
```

Setup the cli tool to create shared test events.

```script
cd event-schema
make dev
```

Run the cli tool to create shared test events, currently just `appsync-authorizer` is supported

```bash
make run
Lambda Name: <Full Lambda Name>
Event Source: appsync-authorizer
```

Ideas:

- [ ] Add cli args
- [ ] Discover the different lambdas and show a list or do code completion
- [ ] Show list of supported event sources
- [ ] Offer some parameters for the event source