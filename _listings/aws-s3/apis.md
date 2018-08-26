---
name: AWS S3
x-slug: aws-s3
description: Amazon Simple Storage Service (Amazon S3) is object storage with a simple
  web service interface to store and retrieve any amount of data from anywhere on
  the web. It is designed to deliver 99.999999999% durability, and scale past trillions
  of objects worldwide.Customers use S3 as a bulk repository, or data lake, for analytics;
  backup &amp; recovery; disaster recovery; and serverless computing. Many cloud-native
  applications even use S3 as primary storage.Its simple to move large volumes of
  data into or out of S3 with Amazonscloud data migrationoptions. Once data is stored
  in Amazon S3, it can be automatically tiered into lower cost, longer-termcloud storageclasses
  like S3 Standard - Infrequent Access and Amazon Glacier for archiving.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Storage-Content-Delivery_AmazonS3.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Bucket ACL
created: "2018-08-25"
modified: "2018-08-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/bucket-acl/master/_listings/aws-s3/apis.md
specificationVersion: "0.14"
apis:
- name: No Title - GET Bucket ACL
  x-api-slug: acl-get
  description: This implementation of the GET operation uses the aclsubresource to
    return the access control list (ACL) of a bucket
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Storage-Content-Delivery_AmazonS3.png
  humanURL: https://aws.amazon.com/s3/
  baseURL: https:////
  tags: Amazon Web Services, Storage, Stack Network, Stack, API Service Provider,
    API Service Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/bucket-acl/master/_listings/aws-s3/acl-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/bucket-acl/master/_listings/aws-s3/acl-get-openapi.md
- name: No Title - PUT Bucket ACL
  x-api-slug: acl-put
  description: This implementation of the PUT operation uses the aclsubresource to
    set the permissions on an existing bucket using access control lists(ACL)
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Storage-Content-Delivery_AmazonS3.png
  humanURL: https://aws.amazon.com/s3/
  baseURL: https:////
  tags: Amazon Web Services, Storage, Stack Network, Stack, API Service Provider,
    API Service Provider, API Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/bucket-acl/master/_listings/aws-s3/acl-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/bucket-acl/master/_listings/aws-s3/acl-put-openapi.md
x-common:
- type: x-api-gallery
  url: http://aws.route.53.api.gallery.streamdata.io
- type: x-api-stack
  url: http://aws.s3.stack.network
- type: x-documentation
  url: http://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html
- type: x-faq
  url: https://aws.amazon.com/s3/faqs/
- type: x-getting-started
  url: https://aws.amazon.com/s3/getting-started/
- type: x-pricing
  url: https://aws.amazon.com/s3/pricing/
- type: x-sla
  url: https://aws.amazon.com/s3/sla/
- type: x-website
  url: https://aws.amazon.com/s3/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---