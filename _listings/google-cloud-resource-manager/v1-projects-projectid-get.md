---
swagger: "2.0"
info:
  title: Google Cloud Resource Manager
  description: The Google Cloud Resource Manager API provides methods for creating,
    reading, and updating project metadata.
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
  /v1/projects/{projectId}:
    get:
      summary: Get Project
      description: |-
        Retrieves the Project identified by the specified
        `project_id` (for example, `my-project-123`)
      operationId: cloudresourcemanager.projects.get
      parameters:
      - in: path
        name: projectId
        description: The Project ID (for example, `my-project-123`)
      responses:
        200:
          description: OK
      tags:
      - project
definitions:
  Ancestor:
    properties: []
  AuditConfig:
    properties:
      auditLogConfigs:
        description: This is a default description.
        type: post
      service:
        description: This is a default description.
        type: post
  AuditLogConfig:
    properties:
      exemptedMembers:
        description: This is a default description.
        type: post
      logType:
        description: This is a default description.
        type: post
  Binding:
    properties:
      members:
        description: This is a default description.
        type: post
      role:
        description: This is a default description.
        type: post
  Empty:
    properties: []
  FolderOperation:
    properties:
      destinationParent:
        description: This is a default description.
        type: post
      displayName:
        description: This is a default description.
        type: post
      operationType:
        description: This is a default description.
        type: post
      sourceParent:
        description: This is a default description.
        type: post
  FolderOperationError:
    properties:
      errorMessageId:
        description: This is a default description.
        type: post
  GetAncestryRequest:
    properties: []
  GetAncestryResponse:
    properties:
      ancestor:
        description: This is a default description.
        type: post
  GetIamPolicyRequest:
    properties: []
  Lien:
    properties:
      createTime:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      origin:
        description: This is a default description.
        type: post
      parent:
        description: This is a default description.
        type: post
      reason:
        description: This is a default description.
        type: post
      restrictions:
        description: This is a default description.
        type: post
  ListLiensResponse:
    properties:
      liens:
        description: This is a default description.
        type: post
      nextPageToken:
        description: This is a default description.
        type: post
  ListProjectsResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: post
      projects:
        description: This is a default description.
        type: post
  Operation:
    properties:
      done:
        description: This is a default description.
        type: post
      metadata:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      response:
        description: This is a default description.
        type: post
  Organization:
    properties:
      creationTime:
        description: This is a default description.
        type: post
      displayName:
        description: This is a default description.
        type: post
      lifecycleState:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
  OrganizationOwner:
    properties:
      directoryCustomerId:
        description: This is a default description.
        type: post
  Policy:
    properties:
      auditConfigs:
        description: This is a default description.
        type: post
      bindings:
        description: This is a default description.
        type: post
      etag:
        description: This is a default description.
        type: post
      version:
        description: This is a default description.
        type: post
  Project:
    properties:
      createTime:
        description: This is a default description.
        type: post
      labels:
        description: This is a default description.
        type: post
      lifecycleState:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      projectId:
        description: This is a default description.
        type: post
      projectNumber:
        description: This is a default description.
        type: post
  ProjectCreationStatus:
    properties:
      createTime:
        description: This is a default description.
        type: post
      gettable:
        description: This is a default description.
        type: post
      ready:
        description: This is a default description.
        type: post
  ResourceId:
    properties:
      id:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  SearchOrganizationsRequest:
    properties:
      filter:
        description: This is a default description.
        type: post
      pageSize:
        description: This is a default description.
        type: post
      pageToken:
        description: This is a default description.
        type: post
  SearchOrganizationsResponse:
    properties:
      nextPageToken:
        description: This is a default description.
        type: post
      organizations:
        description: This is a default description.
        type: post
  SetIamPolicyRequest:
    properties:
      updateMask:
        description: This is a default description.
        type: post
  Status:
    properties:
      code:
        description: This is a default description.
        type: post
      details:
        description: This is a default description.
        type: post
      message:
        description: This is a default description.
        type: post
  TestIamPermissionsRequest:
    properties:
      permissions:
        description: This is a default description.
        type: post
  TestIamPermissionsResponse:
    properties:
      permissions:
        description: This is a default description.
        type: post
  UndeleteProjectRequest:
    properties: []
x-collection-name: Google Cloud Resource Manager
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