# elastic_beanstalk_assignment
Assignment 2.8 for ce9

CLI Commands:

### create new version ###
aws elasticbeanstalk create-application-version \
  --application-name "your-application-name" \
  --version-label "new-version-label" \
  --source-bundle S3Bucket="your-s3-bucket-name",S3Key="path-to-your-bundle.zip" \
  --region "aws-region"

### update environment ###
aws elasticbeanstalk update-environment \
  --environment-name "your-environment-name" \
  --version-label "new-version-label" \
  --region "aws-region"
