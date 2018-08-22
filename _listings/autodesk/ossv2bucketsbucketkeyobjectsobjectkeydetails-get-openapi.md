---
swagger: "2.0"
x-collection-name: Autodesk
x-complete: 0
info:
  title: AutoDesk Forge Get Details
  description: Get details.
  version: 1.0.0
host: developer.api.autodesk.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /authentication/v1/authenticate:
    post:
      summary: Authenticate
      description: Authenticate.
      operationId: AuthenticationV1AuthenticatePost
      x-api-path-slug: authenticationv1authenticate-post
      parameters:
      - in: formData
        name: client_id
      - in: formData
        name: client_secret
      - in: formData
        name: grant_type
      - in: formData
        name: scope
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Authenticate
  /oss/v2/buckets:
    post:
      summary: Create Bucket
      description: Create bucket.
      operationId: OssV2BucketsPost
      x-api-path-slug: ossv2buckets-post
      parameters:
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Bucket
  /oss/v2/buckets/{bucket}/objects/{object}:
    put:
      summary: Upload File
      description: Upload file.
      operationId: OssV2BucketsObjectsByBucketAndObjectPut
      x-api-path-slug: ossv2bucketsbucketobjectsobject-put
      parameters:
      - in: path
        name: bucket
      - in: header
        name: Content-Type
      - in: path
        name: object
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Upload
      - File
  /oss/v2/buckets/{bucketKey}/objects:
    get:
      summary: Get Files
      description: Get files.
      operationId: OssV2BucketsObjectsByBucketKeyGet
      x-api-path-slug: ossv2bucketsbucketkeyobjects-get
      parameters:
      - in: path
        name: bucketKey
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Files
  /oss/v2/buckets/{bucketKey}/objects/{objectKey}/details:
    get:
      summary: Get Details
      description: Get details.
      operationId: OssV2BucketsObjectsDetailsByBucketKeyAndObjectKeyGet
      x-api-path-slug: ossv2bucketsbucketkeyobjectsobjectkeydetails-get
      parameters:
      - in: path
        name: bucketKey
      - in: path
        name: objectKey
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Details
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