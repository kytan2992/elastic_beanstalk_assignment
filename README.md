# elastic_beanstalk_assignment
Assignment 2.8 for ce9

CLI Commands:

### upload file to s3 bucket ###
aws s3 cp /path/to/your/python.zip s3://ky-s3-terraform/python.zip

### create new version ###
aws elasticbeanstalk create-application-version \
  --application-name ky-python-app \
  --version-label 0.0.2 \
  --source-bundle S3Bucket=ky-s3-terraform,S3Key=python.zip \

### update environment ###
aws elasticbeanstalk update-environment \
  --environment-name ky-environment \
  --version-label 0.0.2 \
