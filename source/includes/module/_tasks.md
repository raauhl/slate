# Tasks 

## The Task Object

> THE TASK OBJECT:

```json
{
  "CompanyId": "000123",
  "Id": "TASK001",
  "ProjectId": "PROJ001",
  "ExternalProjectNumber": "EXT001",
  "ExternalId": "EXTTASK001",
  "ExternalDim01": "DIM001",
  "Name": "Install new server",
  "Active": true,
  "StartDate": "2023-05-10T08:00:00Z",
  "FinishedDate": null,
  "EstimatedHourQty": 16.5,
  "ChapterId": 2,
  "ParentActivityId": "PARENT001",
  "IsParent": false,
  "CostPrice": 1200.0,
  "UnitId": 1,
  "MeasureUnitQty": 2.0,
  "Price": 1500.0,
  "FixedResourcePrice": 500.0,
  "WorkDescription": "Install new server in the data center, install software",
  "WorkDescriptionShort": "Install new server in data center",
  "TaskLocationLatitude": 37.7749,
  "TaskLocationLongitude": -122.4194,
  "SafeJobAnalysisApprovalRequired": true,
  "SafeJobAnalysisUserPromptText": "Have you received proper protective equipment for this task?"
}
```

Parameter                      | Type          | Description
------------------------------ | --------------| -----------
CompanyId                      | string        | The unique identifier of the company that owns the project.
Id                             | string        | The unique identifier of the project task.
ProjectId                      | string        | The unique identifier of the project to which the task belongs.
ExternalProjectNumber          | string        | The external project number associated with the task.
ExternalId                     | string        | The external identifier associated with the task.
ExternalDim01                  | string        | The first external dimension associated with the task.
Name                           | string        | The description or name of the task.
Active                         | bool          | Indicates whether the task is active or not.
StartDate                      | DateTime      | The start date of the task.
FinishedDate                   | DateTime?     | The finish date of the task (null if not yet finished).
EstimatedHourQty               | double        | The estimated number of human hours required to complete the task.
ChapterId                      | int           | The identifier of the chapter (if applicable).
ParentActivityId               | string        | The identifier of the parent activity (if applicable).
IsParent                       | bool          | Indicates whether the task is a parent task or not.
CostPrice                      | double        | The cost price of the task.
UnitId                         | int           | The identifier of the unit associated with the task.
MeasureUnitQty                 | double        | The quantity of the measure unit associated with the task.
Price                          | double        | The price of the task.
FixedResourcePrice             | double        | The fixed resource price of the task.
WorkDescription                | string        | The detailed work description of the task.
WorkDescriptionShort           | string        | The short work description of the task.
TaskLocationLatitude           | double?       | The latitude of the task location (null if not applicable).
TaskLocationLongitude          | double?       | The longitude of the task location (null if not applicable).
SafeJobAnalysisApprovalRequired | bool          | Indicates whether Safe Job Analysis approval is required for the task.
SafeJobAnalysisUserPromptText   | string        | The user prompt text for Safe Job Analysis (if applicable).



## Create Task
```shell
curl 
-X POST "http://example.com/​api​/v4​/integration​/tasks" \
-H "accept: text/plain" \
-H "Content-Type: application/json" \
-d '{
  "CompanyId": "000123",
  "Id": "TASK001",
  "ProjectId": "PROJ001",
  "ExternalProjectNumber": "EXT001",
  "ExternalId": "EXTTASK001",
  "ExternalDim01": "DIM001",
  "Name": "Install new server",
  "Active": true,
  "StartDate": "2023-05-10T08:00:00Z",
  "FinishedDate": null,
  "EstimatedHourQty": 16.5,
  "ChapterId": 2,
  "ParentActivityId": "PARENT001",
  "IsParent": false,
  "CostPrice": 1200.0,
  "UnitId": 1,
  "MeasureUnitQty": 2.0,
  "Price": 1500.0,
  "FixedResourcePrice": 500.0,
  "WorkDescription": "Install new server in the data center, install software",
  "WorkDescriptionShort": "Install new server in data center",
  "TaskLocationLatitude": 37.7749,
  "TaskLocationLongitude": -122.4194,
  "SafeJobAnalysisApprovalRequired": true,
  "SafeJobAnalysisUserPromptText": "Have you received proper protective equipment for this task?"
}'
```

This endpoint creates a Task.

### HTTP Request
`POST ​/api​/v4​/integration​/tasks`



## Retrieve Task
```shell
curl 
-X GET "/api/v4/integration/tasks/TASK001" \
-H  "accept: text/plain" 
```

> The above command returns JSON structured like this:

```json
{
  "CompanyId": "000123",
  "Id": "TASK001",
  "ProjectId": "PROJ001",
  "ExternalProjectNumber": "EXT001",
  "ExternalId": "EXTTASK001",
  "ExternalDim01": "DIM001",
  "Name": "Install new server",
  "Active": true,
  "StartDate": "2023-05-10T08:00:00Z",
  "FinishedDate": null,
  "EstimatedHourQty": 16.5,
  "ChapterId": 2,
  "ParentActivityId": "PARENT001",
  "IsParent": false,
  "CostPrice": 1200.0,
  "UnitId": 1,
  "MeasureUnitQty": 2.0,
  "Price": 1500.0,
  "FixedResourcePrice": 500.0,
  "WorkDescription": "Install new server in the data center, install software",
  "WorkDescriptionShort": "Install new server in data center",
  "TaskLocationLatitude": 37.7749,
  "TaskLocationLongitude": -122.4194,
  "SafeJobAnalysisApprovalRequired": true,
  "SafeJobAnalysisUserPromptText": "Have you received proper protective equipment for this task?"
}
```

This endpoint retrieves a Task.

### HTTP Request
`GET /api/v4/integration/tasks/{id}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of a Task inside Ditio.



## Update Task
```shell
curl 
-X PUT "/api/v4/integration/tasks/TASK001" \
-H  "accept: text/plain" 
-d '{
  "CompanyId": "000123",
  "Id": "TASK001",
  "ProjectId": "PROJ001",
  "ExternalProjectNumber": "EXT001",
  "ExternalId": "EXTTASK001",
  "ExternalDim01": "DIM001",
  "Name": "Install new server",
  "Active": true,
  "StartDate": "2023-05-10T08:00:00Z",
  "FinishedDate": null,
  "EstimatedHourQty": 16.5,
  "ChapterId": 3,
  "ParentActivityId": "PARENT001",
  "IsParent": false,
  "CostPrice": 1200.0,
  "UnitId": 1,
  "MeasureUnitQty": 2.0,
  "Price": 1500.0,
  "FixedResourcePrice": 500.0,
  "WorkDescription": "Test the installed Software.",
  "WorkDescriptionShort": "Install new server in data center",
  "TaskLocationLatitude": 37.7749,
  "TaskLocationLongitude": -122.4194,
  "SafeJobAnalysisApprovalRequired": true,
  "SafeJobAnalysisUserPromptText": "Have you received proper training?"
}
```

> The above command returns the updated JSON.

This endpoint updates a Task.

### HTTP Request
`PUT /api/v4/integration/tasks/{id}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of a Task inside Ditio.



## Delete Task
```shell
curl 
-X DELETE "http://example.com/api/v4/integration/tasks/TASK001" 
-H  "accept: */*"
```

This endpoint deletes a Task.

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of a Task inside Ditio.

### HTTP Request
`DELETE /api/v4/integration/tasks/{id}`



## Get All Tasks by Project ID
```shell
curl 
-X GET "http://example.com/api/v4/integration/tasks/project/PROJ001" \
-H  "accept: text/plain"
```

> The above command returns JSON structured like this:

```json
[
  {
    "CompanyId": "000123",
    "Id": "TASK001",
    "ProjectId": "PROJ001",
    "ExternalProjectNumber": "EXT001",
    "ExternalId": "EXTTASK001",
    "ExternalDim01": "DIM001",
    "Name": "Install new server",
    "Active": true,
    "StartDate": "2023-05-10T08:00:00Z",
    "FinishedDate": null,
    "EstimatedHourQty": 16.5,
    "ChapterId": 2,
    "ParentActivityId": "PARENT001",
    "IsParent": false,
    "CostPrice": 1200.0,
    "UnitId": 1,
    "MeasureUnitQty": 2.0,
    "Price": 1500.0,
    "FixedResourcePrice": 500.0,
    "WorkDescription": "Install new server in the data center, install software",
    "WorkDescriptionShort": "Install new server in data center",
    "TaskLocationLatitude": 37.7749,
    "TaskLocationLongitude": -122.4194,
    "SafeJobAnalysisApprovalRequired": true,
    "SafeJobAnalysisUserPromptText": "Have you received proper protective equipment for this task?"
  }
]
```

This endpoint retrieves a list of all tasks in a project by ditio project id

### HTTP Request
`GET /api/v4/integration/projects/{projectId}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of project inside Ditio.



## Get All Tasks by Project Number
```shell
curl 
-X GET "/api/v4/integration/tasks/by-project-number/EXT001" \
-H  "accept: text/plain"
```

> The above command returns JSON structured like this:

```json
[
  {
    "CompanyId": "000123",
    "Id": "TASK001",
    "ProjectId": "PROJ001",
    "ExternalProjectNumber": "EXT001",
    "ExternalId": "EXTTASK001",
    "ExternalDim01": "DIM001",
    "Name": "Install new server",
    "Active": true,
    "StartDate": "2023-05-10T08:00:00Z",
    "FinishedDate": null,
    "EstimatedHourQty": 16.5,
    "ChapterId": 2,
    "ParentActivityId": "PARENT001",
    "IsParent": false,
    "CostPrice": 1200.0,
    "UnitId": 1,
    "MeasureUnitQty": 2.0,
    "Price": 1500.0,
    "FixedResourcePrice": 500.0,
    "WorkDescription": "Install new server in the data center, install software",
    "WorkDescriptionShort": "Install new server in data center",
    "TaskLocationLatitude": 37.7749,
    "TaskLocationLongitude": -122.4194,
    "SafeJobAnalysisApprovalRequired": true,
    "SafeJobAnalysisUserPromptText": "Have you received proper protective equipment for this task?"
  }
]
```

This endpoint retrieves a list of all tasks in a project by project number.

### HTTP Request
`GET /api/v4/integration/tasks/by-project-number/{projectNumber}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
projectNumber | string | The Project Number.



## Get Task in Project
```shell
curl 
-X GET "http://example.com/api/v4/integration/tasks/by-project-number/PROJ001/by-task-number TASK001" \
-H  "accept: text/plain"
```

> The above command returns JSON structured like this:

```json
[
  {
    "CompanyId": "000123",
    "Id": "TASK001",
    "ProjectId": "PROJ001",
    "ExternalProjectNumber": "EXT001",
    "ExternalId": "EXTTASK001",
    "ExternalDim01": "DIM001",
    "Name": "Install new server",
    "Active": true,
    "StartDate": "2023-05-10T08:00:00Z",
    "FinishedDate": null,
    "EstimatedHourQty": 16.5,
    "ChapterId": 2,
    "ParentActivityId": "PARENT001",
    "IsParent": false,
    "CostPrice": 1200.0,
    "UnitId": 1,
    "MeasureUnitQty": 2.0,
    "Price": 1500.0,
    "FixedResourcePrice": 500.0,
    "WorkDescription": "Install new server in the data center, install software",
    "WorkDescriptionShort": "Install new server in data center",
    "TaskLocationLatitude": 37.7749,
    "TaskLocationLongitude": -122.4194,
    "SafeJobAnalysisApprovalRequired": true,
    "SafeJobAnalysisUserPromptText": "Have you received proper protective equipment for this task?"
  }
]
```

This endpoint retrieves a list of all tasks in a project by project number.

### HTTP Request
`GET api/v4/integration/tasks/by-project-number/{projectNumber}/by-task-number/{taskNumber}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
taskNumber | string | The Task Number.
projectNumber | string | The Project Number.



## Get Task By External IDs
```shell
curl 
-X GET "http://example.com/api/v4/integration/tasks/by-project-number/PROJ001/by-task-number TASK001" \
-H  "accept: text/plain"
```

> The above command returns JSON structured like this:

```json
[
  {
    "CompanyId": "000123",
    "Id": "TASK001",
    "ProjectId": "PROJ001",
    "ExternalProjectNumber": "EXT001",
    "ExternalId": "EXTTASK001",
    "ExternalDim01": "DIM001",
    "Name": "Install new server",
    "Active": true,
    "StartDate": "2023-05-10T08:00:00Z",
    "FinishedDate": null,
    "EstimatedHourQty": 16.5,
    "ChapterId": 2,
    "ParentActivityId": "PARENT001",
    "IsParent": false,
    "CostPrice": 1200.0,
    "UnitId": 1,
    "MeasureUnitQty": 2.0,
    "Price": 1500.0,
    "FixedResourcePrice": 500.0,
    "WorkDescription": "Install new server in the data center, install software",
    "WorkDescriptionShort": "Install new server in data center",
    "TaskLocationLatitude": 37.7749,
    "TaskLocationLongitude": -122.4194,
    "SafeJobAnalysisApprovalRequired": true,
    "SafeJobAnalysisUserPromptText": "Have you received proper protective equipment for this task?"
  }
]
```

This endpoint retrieves a list of all tasks in a project by project number.

### HTTP Request
`GET api/v4/integration/tasks/by-project-number/{projectNumber}/by-task-number/{taskNumber}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
taskNumber | string | The Task Number.
projectNumber | string | The Project Number.
