# Gaussian Processes for Cryptocurrency Forecasting

Coming soon!

This cloud architecture is a bit overkill given the small scale usage of this tool, but it is just for learning AWS!

## Main goals

- [x] Scheduled daily EventBridge trigger and Lambda function to fetch and store cryptocurrency data in S3
- [x] Lambda function (triggered by S3 object creation) to transform raw data and copy it to DynamoDB
- [ ] SageMaker training job on new DynamoDB data, storing trained models in S3
- [ ] API Gateway serving SageMaker multi-model endpoint using all historical models in S3
- [ ] Web application for selecting a model and forecast period and displaying predictions

## Refactoring

- [ ] Deploy Lambda functions with dependencies as container images (see [here](https://docs.aws.amazon.com/lambda/latest/dg/images-create.html))

## Side goals

- [ ] Weights & Biases integration for tracking model training and detecting drift
- [ ] SageMaker Studio for direct notebook-like model experimentation
- [ ] ElastiCache / Redis for caching common models and forecast periods.
- [ ] CloudFront for logging