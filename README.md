# Steward S3 Cloud Foundry Broker

   * This repo contains helm charts that will do the following
      * install a configured s3-cf-broker -- https://github.com/cloudfoundry-community/s3-broker
      * install steward cofigured in cf mode pointing at the installed s3-cf-broker
      
# What the heck will this do
   * On create
      * Create an S3 bucket
      * Create an IAM user and grant acccess to the aforementioned bucket
      * Drop bucket-name, AWS_ACCESS_KEY, AWS_SECRET_KEY in a kubernetes secret
      * Secret will look something like this
```yaml
kind: Secret
apiVersion: v1
data:
  name: <base64 enc bucket name>
  password: <AWS_SECRET_KEY>
  username: <AWS_ACCESS_KEY>
```  
      
# Prereqs
   * AWS credentials with full S3 access and access to create and delete users
   * Service name of s3-cf-broker installed in a Kubernetes namespace eg `torpid-skunk-s3-cf-broke.cfbroker.svc.cluster.local`

