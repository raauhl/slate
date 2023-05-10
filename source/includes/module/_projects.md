# Projects

## The Project Object

> THE PROJECT OBJECT:

```json
{
  "companyId": "991123",
  "id": "9911231",
  "projectNumber": "9911231",
  "externalProjectNumber": "EXT-9911231",
  "name": "Highway Construction Project",
  "description": "Construction of a 10-km highway",
  "active": true,
  "blockedForRegistration": false,
  "startDate": "2022-01-01",
  "finishedDatePlanned": "2022-12-31",
  "finishedDate": null,
  "estimatedHourQty": 5000,
  "mainForemanId": "FOREMAN001",
  "projectLeaderId": "LEADER001",
  "mainContactEmail": "contact@constructioncompany.com",
  "workBreakLunchStartTime": "12:00",
  "workBreakLunchLength": 60,
  "workBreakDinnerStartTime": "18:00",
  "workBreakDinnerLength": 30,
  "projectLocationLatitude": 51.5074,
  "projectLocationLongitude": -0.1278
}
```

Parameter          | Type     | Description
------------------ | -------- | -----------
CompanyId          | string   | The unique identifier of the company that owns the machine.
Id                 | string   | The unique identifier of the project.
ProjectNumber      | string   | The unique project number.
ExternalProjectNumber | string | The external project number.
Name               | string   | The name of the project.
Description        | string   | The description of the project.
Active             | bool     | Indicates if the project is currently active.
BlockedForRegistration | bool | Indicates if the project is blocked for registration.
StartDate          | DateTime | The start date of the project.
FinishedDatePlanned| DateTime | The planned finish date of the project.
FinishedDate       | DateTime | The actual finish date of the project.
EstimatedHourQty   | decimal  | The estimated hour quantity for the project.
MainForemanId      | string   | The unique identifier of the main foreman for the project.
ProjectLeaderId    | string   | The unique identifier of the project leader for the project.
MainContactEmail   | string   | The email address of the main contact for the project.
WorkBreakLunchStartTime | TimeSpan | The start time of the lunch break for the project.
WorkBreakLunchLength    | TimeSpan | The length of the lunch break for the project.
WorkBreakDinnerStartTime| TimeSpan | The start time of the dinner break for the project.
WorkBreakDinnerLength   | TimeSpan | The length of the dinner break for the project.
ProjectLocationLatitude | decimal | The latitude coordinate of the project location.
ProjectLocationLongitude| decimal | The longitude coordinate of the project location.



## Create Project
```shell
curl 
-X POST "http://example.com/​api​/v4​/integration​/projects" \
-H "accept: text/plain" \
-H "Content-Type: application/json" \
-d '{
  "companyId": "991123",
  "id": "9911231",
  "projectNumber": "9911231",
  "externalProjectNumber": "EXT-9911231",
  "name": "Highway Construction Project",
  "description": "Construction of a 10-km highway",
  "active": true,
  "blockedForRegistration": false,
  "startDate": "2022-01-01",
  "finishedDatePlanned": "2022-12-31",
  "finishedDate": null,
  "estimatedHourQty": 5000,
  "mainForemanId": "FOREMAN001",
  "projectLeaderId": "LEADER001",
  "mainContactEmail": "contact@constructioncompany.com",
  "workBreakLunchStartTime": "12:00",
  "workBreakLunchLength": 60,
  "workBreakDinnerStartTime": "18:00",
  "workBreakDinnerLength": 30,
  "projectLocationLatitude": 51.5074,
  "projectLocationLongitude": -0.1278
}
```

This endpoint creates a Project.

### HTTP Request
`POST ​/api​/v4​/integration​/projects`



## Retrieve Project
```shell
curl 
-X GET "/api/v4/integration/projects/9911231" \
-H  "accept: text/plain" 
```

> The above command returns JSON structured like this:

```json
{
  "companyId": "991123",
  "id": "9911231",
  "projectNumber": "9911231",
  "externalProjectNumber": "EXT-9911231",
  "name": "Highway Construction Project",
  "description": "Construction of a 10-km highway",
  "active": true,
  "blockedForRegistration": false,
  "startDate": "2022-01-01",
  "finishedDatePlanned": "2022-12-31",
  "finishedDate": null,
  "estimatedHourQty": 5000,
  "mainForemanId": "FOREMAN001",
  "projectLeaderId": "LEADER001",
  "mainContactEmail": "contact@constructioncompany.com",
  "workBreakLunchStartTime": "12:00",
  "workBreakLunchLength": 60,
  "workBreakDinnerStartTime": "18:00",
  "workBreakDinnerLength": 30,
  "projectLocationLatitude": 51.5074,
  "projectLocationLongitude": -0.1278
}
```

This endpoint retrieves a project.

### HTTP Request
`GET /api/v4/integration/projects/{id}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of project inside Ditio.



## Update Project
```shell
curl 
-X PUT "/api/v4/integration/projects/9911231" \
-H  "accept: text/plain" 
-d '{
  "companyId": "991123",
  "id": "9911231",
  "projectNumber": "9911231",
  "externalProjectNumber": "EXT-9911231",
  "name": "Highway Construction Project",
  "description": "Construction of a 10-km highway",
  "active": true,
  "blockedForRegistration": false,
  "startDate": "2022-01-01",
  "finishedDatePlanned": "2022-12-31",
  "finishedDate": null,
  "estimatedHourQty": 5000,
  "mainForemanId": "FOREMAN001",
  "projectLeaderId": "LEADER001",
  "mainContactEmail": "contact@constructioncompany.com",
  "workBreakLunchStartTime": "12:00",
  "workBreakLunchLength": 60,
  "workBreakDinnerStartTime": "18:00",
  "workBreakDinnerLength": 30,
  "projectLocationLatitude": 51.5074,
  "projectLocationLongitude": -0.1278
}
```

> The above command returns the updated JSON.

This endpoint updates a project.

### HTTP Request
`PUT /api/v4/integration/projects/{id}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of project inside Ditio.



## Delete Project
```shell
curl 
-X DELETE "http://example.com/api/v4/integration/projects/342342" 
-H  "accept: */*"
```

This endpoint deletes the project.

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of project inside Ditio.

### HTTP Request
`DELETE /api/v4/integration/projects/{id}`



## Get All Projects
```shell
curl 
-X GET "http://example.com/api/v4/integration/projects" \
-H  "accept: text/plain"
```

> The above command returns JSON structured like this:

```json
[
  {
    "companyId": "991123",
    "id": "9911231",
    "projectNumber": "9911231",
    "externalProjectNumber": "EXT-9911231",
    "name": "Highway Construction Project",
    "description": "Construction of a 10-km highway",
    "active": true,
    "blockedForRegistration": false,
    "startDate": "2022-01-01",
    "finishedDatePlanned": "2022-12-31",
    "finishedDate": null,
    "estimatedHourQty": 5000,
    "mainForemanId": "FOREMAN001",
    "projectLeaderId": "LEADER001",
    "mainContactEmail": "contact@constructioncompany.com",
    "workBreakLunchStartTime": "12:00",
    "workBreakLunchLength": 60,
    "workBreakDinnerStartTime": "18:00",
    "workBreakDinnerLength": 30,
    "projectLocationLatitude": 51.5074,
    "projectLocationLongitude": -0.1278
  }
]
```

This endpoint retrieves all the projects.

### HTTP Request
`GET /api/v4/integration/projects`



## Get Project By Number
```shell
curl 
-X GET "http://example.com//api/v4/integration/projects/by-project-number/23}" \
-H  "accept: text/plain"
```

> The above command returns JSON structured like this:

```json
{
  "companyId": "991123",
  "id": "9911231",
  "projectNumber": "23",
  "externalProjectNumber": "EXT-9911231",
  "name": "Highway Construction Project",
  "description": "Construction of a 10-km highway",
  "active": true,
  "blockedForRegistration": false,
  "startDate": "2022-01-01",
  "finishedDatePlanned": "2022-12-31",
  "finishedDate": null,
  "estimatedHourQty": 5000,
  "mainForemanId": "FOREMAN001",
  "projectLeaderId": "LEADER001",
  "mainContactEmail": "contact@constructioncompany.com",
  "workBreakLunchStartTime": "12:00",
  "workBreakLunchLength": 60,
  "workBreakDinnerStartTime": "18:00",
  "workBreakDinnerLength": 30,
  "projectLocationLatitude": 51.5074,
  "projectLocationLongitude": -0.1278
}
```

This endpoint gets a project by the project number.

### HTTP Request
`GET /api/v4/integration/projects/by-project-number/{projectNumber}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
projectNumber | string | External Project Number.
