{
  "info": {
    "name": "Google Cloud Resource Manager API List Liens",
    "_postman_id": "0ab78e12-afa4-49c0-a79c-51c909853dc9",
    "description": "List all Liens applied to the `parent` resource.\n\nCallers of this method will require permission on the `parent` resource.\nFor example, a Lien with a `parent` of `projects/1234` requires permission\n`resourcemanager.projects.get`.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Lien",
      "item": [
        {
          "id": "2ba0bea1-f1d6-4065-81c8-a1b1e7c0c919",
          "name": "cloudresourcemanager.liens.list",
          "request": {
            "url": "http://cloudresourcemanager.googleapis.com/v1/liens?pageSize=%7B%7D&pageToken=%7B%7D&parent=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List all Liens applied to the `parent` resource.\n\nCallers of this method will require permission on the `parent` resource.\nFor example, a Lien with a `parent` of `projects/1234` requires permission\n`resourcemanager.projects.get`."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "0b4d4c38-3e49-46b6-b56b-cb5870ef49be"
            }
          ]
        }
      ]
    }
  ]
}