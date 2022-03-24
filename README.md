# Gaussian Processes for Cryptocurrency Forecasting

Coming soon!

This cloud architecture is a bit overkill given the likely small scale usage of this tool, but it is an interesting way to learn about AWS services.

## Main goals

- [x] Scheduled daily EventBridge trigger and Lambda function to fetch and store cryptocurrency data in S3
- [x] Lambda function (triggered by S3 object creation) to transform raw data and copy it to DynamoDB
- [ ] SageMaker training job on new DynamoDB data, storing trained models on S3
- [ ] API Gateway serving SageMaker multi-model endpoint using all historical models on S3
- [ ] Web application for selecting a model and forecast period and displaying predictions

## Other

- [ ] Weights & Biases integration for tracking model training and detecting concept drift
- [ ] SageMaker Studio for direct notebook-like model experimentation
- [ ] ElastiCache for caching common models and forecast periods.
- [ ] CloudFront for logging