---
swagger: "2.0"
x-collection-name: Google Cloud Resource Manager
x-complete: 0
info:
  title: Google Cloud Resource Manager API Delete Project
  description: |-
    Marks the Project identified by the specified
    `project_id` (for example, `my-project-123`) for deletion.
    This method will only affect the Project if the following criteria are met:

    + The Project does not have a billing account associated with it.
    + The Project has a lifecycle state of
    ACTIVE.

    This method changes the Project's lifecycle state from
    ACTIVE
    to DELETE_REQUESTED.
    The deletion starts at an unspecified time,
    at which point the Project is no longer accessible.

    Until the deletion completes, you can check the lifecycle state
    checked by retrieving the Project with GetProject,
    and the Project remains visible to ListProjects.
    However, you cannot update the project.

    After the deletion completes, the Project is not retrievable by
    the  GetProject and
    ListProjects methods.

    The caller must have modify permissions for this Project.
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
    post:
      summary: Create Project
      description: |-
        Request that a new Project be created. The result is an Operation which
        can be used to track the creation process. It is automatically deleted
        after a few hours, so there is no need to call DeleteOperation.

        Our SLO permits Project creation to take up to 30 seconds at the 90th
        percentile. As of 2016-08-29, we are observing 6 seconds 50th percentile
        latency. 95th percentile latency is around 11 seconds. We recommend
        polling at the 5th second with an exponential backoff.
      operationId: cloudresourcemanager.projects.create
      x-api-path-slug: v1projects-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Project
  /v1/projects/{projectId}:
    delete:
      summary: Delete Project
      description: |-
        Marks the Project identified by the specified
        `project_id` (for example, `my-project-123`) for deletion.
        This method will only affect the Project if the following criteria are met:

        + The Project does not have a billing account associated with it.
        + The Project has a lifecycle state of
        ACTIVE.

        This method changes the Project's lifecycle state from
        ACTIVE
        to DELETE_REQUESTED.
        The deletion starts at an unspecified time,
        at which point the Project is no longer accessible.

        Until the deletion completes, you can check the lifecycle state
        checked by retrieving the Project with GetProject,
        and the Project remains visible to ListProjects.
        However, you cannot update the project.

        After the deletion completes, the Project is not retrievable by
        the  GetProject and
        ListProjects methods.

        The caller must have modify permissions for this Project.
      operationId: cloudresourcemanager.projects.delete
      x-api-path-slug: v1projectsprojectid-delete
      parameters:
      - in: path
        name: projectId
        description: The Project ID (for example, `foo-bar-123`)
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