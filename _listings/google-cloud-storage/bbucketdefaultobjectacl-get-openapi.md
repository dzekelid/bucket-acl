---
swagger: "2.0"
x-collection-name: Google Cloud Storage
x-complete: 0
info:
  title: Google Cloud Storage Get Bucket Default ACL
  version: 1.0.0
  description: Retrieves default object ACL entries on the specified bucket.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /b/{bucket}/acl:
    get:
      summary: Get Bucket ACLs
      description: Retrieves ACL entries on the specified bucket.
      operationId: storage.bucketAccessControls.list
      x-api-path-slug: bbucketacl-get
      parameters:
      - in: path
        name: bucket
        description: Name of a bucket
      responses:
        200:
          description: OK
      tags:
      - Bucket ACL
    post:
      summary: Create Bucket ACL
      description: Creates a new ACL entry on the specified bucket.
      operationId: storage.bucketAccessControls.insert
      x-api-path-slug: bbucketacl-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: bucket
        description: Name of a bucket
      responses:
        200:
          description: OK
      tags:
      - Bucket ACL
  /b/{bucket}/acl/{entity}:
    delete:
      summary: Delete Bucket ACL
      description: Permanently deletes the ACL entry for the specified entity on the
        specified bucket.
      operationId: storage.bucketAccessControls.delete
      x-api-path-slug: bbucketaclentity-delete
      parameters:
      - in: path
        name: bucket
        description: Name of a bucket
      - in: path
        name: entity
        description: The entity holding the permission
      responses:
        200:
          description: OK
      tags:
      - Bucket ACL
    get:
      summary: Get Bucket ACL
      description: Returns the ACL entry for the specified entity on the specified
        bucket.
      operationId: storage.bucketAccessControls.get
      x-api-path-slug: bbucketaclentity-get
      parameters:
      - in: path
        name: bucket
        description: Name of a bucket
      - in: path
        name: entity
        description: The entity holding the permission
      responses:
        200:
          description: OK
      tags:
      - Bucket ACL
    patch:
      summary: Update Bucket ACL
      description: Updates an ACL entry on the specified bucket. This method supports
        patch semantics.
      operationId: storage.bucketAccessControls.patch
      x-api-path-slug: bbucketaclentity-patch
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: bucket
        description: Name of a bucket
      - in: path
        name: entity
        description: The entity holding the permission
      responses:
        200:
          description: OK
      tags:
      - Bucket ACL
    put:
      summary: Update Bucket ACL
      description: Updates an ACL entry on the specified bucket.
      operationId: storage.bucketAccessControls.update
      x-api-path-slug: bbucketaclentity-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: bucket
        description: Name of a bucket
      - in: path
        name: entity
        description: The entity holding the permission
      responses:
        200:
          description: OK
      tags:
      - Bucket ACL
  /b/{bucket}/defaultObjectAcl:
    get:
      summary: Get Bucket Default ACL
      description: Retrieves default object ACL entries on the specified bucket.
      operationId: storage.defaultObjectAccessControls.list
      x-api-path-slug: bbucketdefaultobjectacl-get
      parameters:
      - in: path
        name: bucket
        description: Name of a bucket
      - in: query
        name: ifMetagenerationMatch
        description: If present, only return default ACL listing if the buckets current
          metageneration matches this value
      - in: query
        name: ifMetagenerationNotMatch
        description: If present, only return default ACL listing if the buckets current
          metageneration does not match the given value
      responses:
        200:
          description: OK
      tags:
      - Bucket ACL
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---