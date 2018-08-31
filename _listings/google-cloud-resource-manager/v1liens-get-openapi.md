---
swagger: "2.0"
x-collection-name: Google Cloud Resource Manager
x-complete: 0
info:
  title: Google Cloud Resource Manager API List Liens
  description: |-
    List all Liens applied to the `parent` resource.

    Callers of this method will require permission on the `parent` resource.
    For example, a Lien with a `parent` of `projects/1234` requires permission
    `resourcemanager.projects.get`.
  contact:
    name: Google
    url: https://google.com
  version: v1
host: cloudresourcemanager.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/liens:
    get:
      summary: List Liens
      description: |-
        List all Liens applied to the `parent` resource.

        Callers of this method will require permission on the `parent` resource.
        For example, a Lien with a `parent` of `projects/1234` requires permission
        `resourcemanager.projects.get`.
      operationId: cloudresourcemanager.liens.list
      x-api-path-slug: v1liens-get
      parameters:
      - in: query
        name: pageSize
        description: The maximum number of items to return
      - in: query
        name: pageToken
        description: The `next_page_token` value returned from a previous List request,
          if any
      - in: query
        name: parent
        description: The name of the resource to list all attached Liens
      responses:
        200:
          description: OK
      tags:
      - Lien
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