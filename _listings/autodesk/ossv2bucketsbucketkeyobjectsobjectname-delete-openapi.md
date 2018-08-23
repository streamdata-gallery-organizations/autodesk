---
swagger: "2.0"
x-collection-name: Autodesk
x-complete: 0
info:
  title: AutoDesk Forge Delete File
  description: Delete file.
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
  /modelderivative/v2/designdata/formats:
    get:
      summary: Get Formats
      description: Get formats.
      operationId: ModelderivativeV2DesigndataFormatsGet
      x-api-path-slug: modelderivativev2designdataformats-get
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Formats
  /modelderivative/v2/designdata/job:
    post:
      summary: Post Job obj
      description: Post job obj.
      operationId: ModelderivativeV2DesigndataJobPost3
      x-api-path-slug: modelderivativev2designdatajob-post
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
      - Job
      - Obj
  /modelderivative/v2/designdata/{urn}/manifest:
    get:
      summary: Get Manifest
      description: Get manifest.
      operationId: ModelderivativeV2DesigndataManifestByUrnGet
      x-api-path-slug: modelderivativev2designdataurnmanifest-get
      parameters:
      - in: path
        name: urn
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Manifest
    delete:
      summary: Delete Manifest
      description: Delete manifest.
      operationId: ModelderivativeV2DesigndataManifestByUrnDelete
      x-api-path-slug: modelderivativev2designdataurnmanifest-delete
      parameters:
      - in: path
        name: urn
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Manifest
  /modelderivative/v2/designdata/{urn}/metadata:
    get:
      summary: Get Metadata
      description: Get metadata.
      operationId: ModelderivativeV2DesigndataMetadataByUrnGet
      x-api-path-slug: modelderivativev2designdataurnmetadata-get
      parameters:
      - in: path
        name: urn
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Metadata
  /modelderivative/v2/designdata/{urn}/metadata/{guid}:
    get:
      summary: Get Hierarchy
      description: Get hierarchy.
      operationId: ModelderivativeV2DesigndataMetadataByUrnAndGuidGet
      x-api-path-slug: modelderivativev2designdataurnmetadataguid-get
      parameters:
      - in: path
        name: guid
      - in: path
        name: urn
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Hierarchy
  /modelderivative/v2/designdata/{urn}/metadata/{guid}/properties:
    get:
      summary: Get Properties
      description: Get properties.
      operationId: ModelderivativeV2DesigndataMetadataPropertiesByUrnAndGuidGet
      x-api-path-slug: modelderivativev2designdataurnmetadataguidproperties-get
      parameters:
      - in: path
        name: guid
      - in: path
        name: urn
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Properties
  /modelderivative/v2/designdata/{urn}/thumbnail:
    get:
      summary: Get Thumbnail
      description: Get thumbnail.
      operationId: ModelderivativeV2DesigndataThumbnailByUrnGet
      x-api-path-slug: modelderivativev2designdataurnthumbnail-get
      parameters:
      - in: path
        name: urn
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - Thumbnail
  /oss/v2/buckets/{bucketKey}/objects/{objectName}:
    delete:
      summary: Delete File
      description: Delete file.
      operationId: OssV2BucketsObjectsByBucketKeyAndObjectNameDelete
      x-api-path-slug: ossv2bucketsbucketkeyobjectsobjectname-delete
      parameters:
      - in: path
        name: bucketKey
      - in: path
        name: objectName
      responses:
        200:
          description: OK
      tags:
      - AutoCad
      - File
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