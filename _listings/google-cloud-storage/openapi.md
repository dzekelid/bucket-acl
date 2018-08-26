---
swagger: "2.0"
x-collection-name: Google Cloud Storage
x-complete: 1
info:
  title: Google Cloud Storage
  version: 1.0.0
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
    post:
      summary: Create Bucket Default ACL
      description: Creates a new default object ACL entry on the specified bucket.
      operationId: storage.defaultObjectAccessControls.insert
      x-api-path-slug: bbucketdefaultobjectacl-post
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
  /b/{bucket}/defaultObjectAcl/{entity}:
    delete:
      summary: Default Bucket Default ACL
      description: Permanently deletes the default object ACL entry for the specified
        entity on the specified bucket.
      operationId: storage.defaultObjectAccessControls.delete
      x-api-path-slug: bbucketdefaultobjectaclentity-delete
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
      summary: Get Bucket Default ACL
      description: Returns the default object ACL entry for the specified entity on
        the specified bucket.
      operationId: storage.defaultObjectAccessControls.get
      x-api-path-slug: bbucketdefaultobjectaclentity-get
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
      summary: Update Bucket Default ACL
      description: Updates a default object ACL entry on the specified bucket. This
        method supports patch semantics.
      operationId: storage.defaultObjectAccessControls.patch
      x-api-path-slug: bbucketdefaultobjectaclentity-patch
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
      summary: Update Bucket Default ACL
      description: Updates a default object ACL entry on the specified bucket.
      operationId: storage.defaultObjectAccessControls.update
      x-api-path-slug: bbucketdefaultobjectaclentity-put
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
---