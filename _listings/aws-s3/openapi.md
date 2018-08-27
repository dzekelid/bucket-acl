swagger: "2.0"
x-collection-name: AWS S3
x-complete: 1
info:
  title: No Title
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?acl:
    get:
      summary: GET Bucket ACL
      description: This implementation of the GET operation uses the aclsubresource
        to return the access control list (ACL) of a bucket
      operationId: get-bucket-acl
      x-api-path-slug: acl-get
      responses:
        200:
          description: OK
      tags:
      - Bucket
      - ACL
    put:
      summary: PUT Bucket ACL
      description: This implementation of the PUT operation uses the aclsubresource
        to set the permissions on an existing bucket using access control lists(ACL)
      operationId: put-bucket-acl
      x-api-path-slug: acl-put
      parameters:
      - in: header
        name: x-amz-acl
        description: Sets the ACL of the bucket using the specified canned ACL
      - in: header
        name: x-amz-grant-full-control
        description: Allows the specified grantee(s) the READ, WRITE, READ_ACP, and
          WRITE_ACPtttttttttpermissions on the bucket
      - in: header
        name: x-amz-grant-read
        description: Allows the specified grantee(s) to list the objects in the bucket
      - in: header
        name: x-amz-grant-read-acp
        description: Allows the specified grantee(s) to read the bucket ACL
      - in: header
        name: x-amz-grant-write
        description: Allows the specified grantee(s) to create, overwrite, and delete
          any object in thetttttttttbucket
      - in: header
        name: x-amz-grant-write-acp
        description: Allows the specified grantee(s) to write the ACL for the applicabletttttttttbucket
      responses:
        200:
          description: OK
      tags:
      - Bucket
      - ACL