---
swagger: "2.0"
x-collection-name: Docsmore
x-complete: 0
info:
  title: Docsmore Get Workflow Link For Flow Track
  description: |-
    In Docsmore space, Flow Track means all the client documents generated using one of the Document Flow. In other words, it is an instance of Document FLow. The other thing to notice here is payload information is remarkably similar to general "Workflow" of a Single Document.

    When you initiate this API call, you are basically setting up a new instance of Workflow and in turn getting workflow link of the starting document in the workflow.

    If "flowtrackid" value is "new", then new flowtrack will be created. If flowtrackid has a value of actual flowtrackid then link will be provided to access read-only view of document flowtrack
  version: "1.0"
host: api.docsmore.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/docflowtracks/flowtrackviaapi:
    post:
      summary: Get Workflow Link For Flow Track
      description: |-
        In Docsmore space, Flow Track means all the client documents generated using one of the Document Flow. In other words, it is an instance of Document FLow. The other thing to notice here is payload information is remarkably similar to general "Workflow" of a Single Document.

        When you initiate this API call, you are basically setting up a new instance of Workflow and in turn getting workflow link of the starting document in the workflow.

        If "flowtrackid" value is "new", then new flowtrack will be created. If flowtrackid has a value of actual flowtrackid then link will be provided to access read-only view of document flowtrack
      operationId: ApiDocflowtracksFlowtrackviaapiPost
      x-api-path-slug: apidocflowtracksflowtrackviaapi-post
      parameters:
      - in: header
        name: Accept
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
      - Workflow
      - Link
      - Flow
      - Track
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