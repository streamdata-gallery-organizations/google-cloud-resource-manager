---
name: Google Cloud Resource Manager
x-slug: google-cloud-resource-manager
description: Google Cloud Platform provides resource containers such as Organizations
  and Projects, that allow you to group and hierarchically organize other Cloud Platform
  resources. This hierarchical organization lets you easily manage common aspects
  of your resources such as access control and configuration settings. The Google
  Cloud Resource Manager service enables you to programmatically manage these resource
  containers.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
x-kinRank: "9"
x-alexaRank: ""
tags: Google Cloud Resource Manager
created: "2018-05-21"
modified: "2018-05-21"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/apis.md
specificationVersion: "0.14"
apis:
- name: Google Cloud Resource Manager API List Liens
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    List all Liens applied to the `parent` resource.

    Callers of this method will require permission on the `parent` resource.
    For example, a Lien with a `parent` of `projects/1234` requires permission
    `resourcemanager.projects.get`.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/liens
  tags: Lien
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1liens-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1liens-get-openapi.md
- name: Google Cloud Resource Manager API Create Lien
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Create a Lien which applies to the resource denoted by the `parent` field.

    Callers of this method will require permission on the `parent` resource.
    For example, applying to `projects/1234` requires permission
    `resourcemanager.projects.updateLiens`.

    NOTE: Some resources may limit the number of Liens which may be applied.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/liens
  tags: Lien
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1liens-post-openapi.md
- name: Google Cloud Resource Manager API Search Organization
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Searches Organization resources that are visible to the user and satisfy
    the specified filter. This method returns Organizations in an unspecified
    order. New Organizations do not necessarily appear at the end of the
    results.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/organizations:search
  tags: Organization
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1organizationssearch-post-openapi.md
- name: Google Cloud Resource Manager API List Projects
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Lists Projects that are visible to the user and satisfy the
    specified filter. This method returns Projects in an unspecified order.
    New Projects do not necessarily appear at the end of the list.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/projects
  tags: Project
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1projects-get-openapi.md
- name: Google Cloud Resource Manager API Create Project
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Request that a new Project be created. The result is an Operation which
    can be used to track the creation process. It is automatically deleted
    after a few hours, so there is no need to call DeleteOperation.

    Our SLO permits Project creation to take up to 30 seconds at the 90th
    percentile. As of 2016-08-29, we are observing 6 seconds 50th percentile
    latency. 95th percentile latency is around 11 seconds. We recommend
    polling at the 5th second with an exponential backoff.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/projects
  tags: Project
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1projects-post-openapi.md
- name: Google Cloud Resource Manager API Delete Project
  x-api-slug: google-cloud-resource-manager-api
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
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/projects/{projectId}
  tags: Project
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1projectsprojectid-delete-openapi.md
- name: Google Cloud Resource Manager API Get Project
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Retrieves the Project identified by the specified
    `project_id` (for example, `my-project-123`).

    The caller must have read permissions for this Project.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/projects/{projectId}
  tags: Project
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1projectsprojectid-get-openapi.md
- name: Google Cloud Resource Manager API Update Project
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Updates the attributes of the Project identified by the specified
    `project_id` (for example, `my-project-123`).

    The caller must have modify permissions for this Project.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/projects/{projectId}
  tags: Project
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1projectsprojectid-put-openapi.md
- name: Google Cloud Resource Manager API Get Project Ancestry
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Gets a list of ancestors in the resource hierarchy for the Project
    identified by the specified `project_id` (for example, `my-project-123`).

    The caller must have read permissions for this Project.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/projects/{projectId}:getAncestry
  tags: Project
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1projectsprojectidgetancestry-post-openapi.md
- name: Google Cloud Resource Manager API Restore Project
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Restores the Project identified by the specified
    `project_id` (for example, `my-project-123`).
    You can only use this method for a Project that has a lifecycle state of
    DELETE_REQUESTED.
    After deletion starts, the Project cannot be restored.

    The caller must have modify permissions for this Project.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/projects/{projectId}:undelete
  tags: Project
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1projectsprojectidundelete-post-openapi.md
- name: Google Cloud Resource Manager API Get IAM Policy
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Returns the IAM access control policy for the specified Project.
    Permission is denied if the policy or the resource does not exist.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/projects/{resource}:getIamPolicy
  tags: IAM
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1projectsresourcegetiampolicy-post-openapi.md
- name: Google Cloud Resource Manager API Set IAM Policy
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Sets the IAM access control policy for the specified Project. Replaces
    any existing policy.

    The following constraints apply when using `setIamPolicy()`:

    + Project does not support `allUsers` and `allAuthenticatedUsers` as
    `members` in a `Binding` of a `Policy`.

    + The owner role can be granted only to `user` and `serviceAccount`.

    + Service accounts can be made owners of a project directly
    without any restrictions. However, to be added as an owner, a user must be
    invited via Cloud Platform console and must accept the invitation.

    + A user cannot be granted the owner role using `setIamPolicy()`. The user
    must be granted the owner role using the Cloud Platform Console and must
    explicitly accept the invitation.

    + Invitations to grant the owner role cannot be sent using
    `setIamPolicy()`;
    they must be sent only using the Cloud Platform Console.

    + Membership changes that leave the project without any owners that have
    accepted the Terms of Service (ToS) will be rejected.

    + There must be at least one owner who has accepted the Terms of
    Service (ToS) agreement in the policy. Calling `setIamPolicy()` to
    to remove the last ToS-accepted owner from the policy will fail. This
    restriction also applies to legacy projects that no longer have owners
    who have accepted the ToS. Edits to IAM policies will be rejected until
    the lack of a ToS-accepting owner is rectified.

    + Calling this method requires enabling the App Engine Admin API.

    Note: Removing service accounts from policies or changing their roles
    can render services completely inoperable. It is important to understand
    how the service account is being used before removing or updating its
    roles.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/projects/{resource}:setIamPolicy
  tags: IAM
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1projectsresourcesetiampolicy-post-openapi.md
- name: Google Cloud Resource Manager API Test IAM Policy
  x-api-slug: google-cloud-resource-manager-api
  description: Returns permissions that a caller has on the specified Project.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/projects/{resource}:testIamPermissions
  tags: IAM
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1projectsresourcetestiampermissions-post-openapi.md
- name: Google Cloud Resource Manager API Delete Lien
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Delete a Lien by `name`.

    Callers of this method will require permission on the `parent` resource.
    For example, a Lien with a `parent` of `projects/1234` requires permission
    `resourcemanager.projects.updateLiens`.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/{name}
  tags: Lien
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1name-delete-openapi.md
- name: Google Cloud Resource Manager API Get Operation
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Gets the latest state of a long-running operation.  Clients can use this
    method to poll the operation result at intervals as recommended by the API
    service.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/{name}
  tags: Operation
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1name-get-openapi.md
- name: Google Cloud Resource Manager API Get Organization IAM Policy
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Gets the access control policy for an Organization resource. May be empty
    if no such policy or resource exists. The `resource` field should be the
    organization's resource name, e.g. "organizations/123".
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/{resource}:getIamPolicy
  tags: Organization
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1resourcegetiampolicy-post-openapi.md
- name: Google Cloud Resource Manager API Set Organization IAM Policy
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Sets the access control policy on an Organization resource. Replaces any
    existing policy. The `resource` field should be the organization's resource
    name, e.g. "organizations/123".
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/{resource}:setIamPolicy
  tags: Organization
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1resourcesetiampolicy-post-openapi.md
- name: Google Cloud Resource Manager API TEst Organization IAM Permissions
  x-api-slug: google-cloud-resource-manager-api
  description: |-
    Returns permissions that a caller has on the specified Organization.
    The `resource` field should be the organization's resource name,
    e.g. "organizations/123".
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com////v1/{resource}:testIamPermissions
  tags: Organization
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/v1resourcetestiampermissions-post-openapi.md
- name: Google Cloud Resource Manager API
  x-api-slug: google-cloud-resource-manager-api
  description: Google Cloud Platform provides resource containers such as Organizations
    and Projects, that allow you to group and hierarchically organize other Cloud
    Platform resources. This hierarchical organization lets you easily manage common
    aspects of your resources such as access control and configuration settings. The
    Google Cloud Resource Manager service enables you to programmatically manage these
    resource containers.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Generic-GCP.png
  humanURL: https://cloud.google.com/resource-manager/
  baseURL: ://cloudresourcemanager.googleapis.com//
  tags: Google Cloud Resource Manager
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-cloud-resource-manager/master/_listings/google-cloud-resource-manager/openapi.md
x-common:
- type: x-authentication
  url: https://cloud.google.com/resource-manager/docs/authorizing
- type: x-code
  url: https://cloud.google.com/resource-manager/docs/libraries
- type: x-documentation
  url: https://cloud.google.com/resource-manager/docs/
- type: x-errors
  url: https://cloud.google.com/resource-manager/docs/core_errors
- type: x-how-to-guides
  url: https://cloud.google.com/resource-manager/docs/how-to
- type: x-performance
  url: https://cloud.google.com/resource-manager/docs/performance
- type: x-pricing
  url: https://cloud.google.com/resource-manager/pricing
- type: x-rate-limits
  url: https://cloud.google.com/resource-manager/docs/limits
- type: x-website
  url: https://cloud.google.com/resource-manager/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---