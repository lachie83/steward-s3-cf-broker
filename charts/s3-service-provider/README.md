helm install . --namespace=cfbroker --set AdminAwsAccessKeyId=${AWS_ACCESS_KEY},AdminAwsSecretAccessKey=${AWS_SECRET_KEY} --name s3-provider --namespace steward --replace
