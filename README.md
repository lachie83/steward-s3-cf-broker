# Steward S3 CloudFoundary Broker

   * This repo contains helm charts that will do the following
      * install a configured s3-cf-broker -- https://github.com/cloudfoundry-community/s3-broker
      * install steward cofigured in cf mode pointing at the installed s3-cf-broker
      
# Prereqs
   * AWS credentials with full S3 access
   * Service name of s3-cf-broker installed in a Kubernetes namespace eg `torpid-skunk-s3-cf-broke.cfbroker.svc.cluster.local`

