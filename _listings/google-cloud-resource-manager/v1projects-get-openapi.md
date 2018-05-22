---
swagger: "2.0"
x-collection-name: Google Cloud Resource Manager
x-complete: 0
info:
  title: Google Cloud Resource Manager API List Projects
  description: |-
    Lists Projects that are visible to the user and satisfy the
    specified filter. This method returns Projects in an unspecified order.
    New Projects do not necessarily appear at the end of the list.
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
    post:
      summary: Create Lien
      description: |-
        Create a Lien which applies to the resource denoted by the `parent` field.

        Callers of this method will require permission on the `parent` resource.
        For example, applying to `projects/1234` requires permission
        `resourcemanager.projects.updateLiens`.

        NOTE: Some resources may limit the number of Liens which may be applied.
      operationId: cloudresourcemanager.liens.create
      x-api-path-slug: v1liens-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Lien
  /v1/organizations:search:
    post:
      summary: Search Organization
      description: |-
        Searches Organization resources that are visible to the user and satisfy
        the specified filter. This method returns Organizations in an unspecified
        order. New Organizations do not necessarily appear at the end of the
        results.
      operationId: cloudresourcemanager.organizations.search
      x-api-path-slug: v1organizationssearch-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Organization
  /v1/projects:
    get:
      summary: List Projects
      description: |-
        Lists Projects that are visible to the user and satisfy the
        specified filter. This method returns Projects in an unspecified order.
        New Projects do not necessarily appear at the end of the list.
      operationId: cloudresourcemanager.projects.list
      x-api-path-slug: v1projects-get
      parameters:
      - in: query
        name: filter
        description: An expression for filtering the results of the request
      - in: query
        name: pageSize
        description: The maximum number of Projects to return in the response
      - in: query
        name: pageToken
        description: A pagination token returned from a previous call to ListProjectsthat
          indicates from where listing should continue
      responses:
        200:
          description: OK
      tags:
      - Project
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