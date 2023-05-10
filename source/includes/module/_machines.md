# Machines

## The Machine Object

> THE MACHINE OBJECT:

```json
{
  "companyId": "991123",
  "id": "9911231",
  "machineNumber": "9911231",
  "department": "Manufacturing",
  "name": "High-Performance Milling Machine",
  "typeId": "MILL001",
  "costPriceMachine": 50000,
  "costPrice": 75000,
  "price": 100000,
  "weight": 2500,
  "capacity": 1500,
  "note": "This machine requires special training to operate.",
  "active": true,
  "buildYear": 2019,
  "emissionClass": null,
  "hourMeter": 500,
  "serviceDate": "2023-04-15T10:30:00.000Z",
  "serialNumber": "SERIAL001",
  "engineNumber": null,
  "registrationNumber": null,
  "responsibleId": "EMP001",
  "responsibleEmployeeNumber": "E001",
  "isEquipment": true
}
```

Parameter        | Type      | Description
---------------- | ---------| -----------
companyId        | string   | The unique identifier of the company that owns the machine.
id               | string   | The unique identifier of the machine.
machineNumber    | string   | The unique identifier of the machine.
department       | string   | The department or location where the machine is located.
name             | string   | The name of the machine.
typeId           | string   | The unique identifier of the machine type.
costPriceMachine | number   | The cost price of the machine itself (excluding any attachments).
costPrice        | number   | The total cost price of the machine including any attachments.
price            | number   | The selling price of the machine.
weight           | number   | The weight of the machine (in kilograms).
capacity         | number   | The capacity of the machine (in liters, cubic meters, etc.).
note             | string   | Additional notes or comments about the machine.
active           | boolean  | Indicates whether the machine is currently active.
buildYear        | number   | The year in which the machine was built.
emissionClass    | string   | The emission class of the machine (if applicable).
hourMeter        | number   | The total number of hours the machine has been in operation.
serviceDate      | string   | The date of the last service or maintenance check on the machine.
serialNumber     | string   | The serial number of the machine (if applicable).
engineNumber     | string   | The engine number of the machine (if applicable).
registrationNumber | string | The registration number of the machine (if applicable).
responsibleId    | string   | The unique identifier of the employee responsible for the machine.
responsibleEmployeeNumber | string | The employee number of the employee responsible for the machine.
isEquipment      | boolean  | Indicates whether the machine is classified as equipment.



## Create Machine
```shell
curl 
-X POST "http://example.com/api/v4/integration/machines" \
-H "accept: text/plain" \
-H "Content-Type: application/json" \
-d '{
  "companyId": "991123",
  "id": "9911231",
  "machineNumber": "9911231",
  "department": "Manufacturing",
  "name": "High-Performance Milling Machine",
  "typeId": "MILL001",
  "costPriceMachine": 50000,
  "costPrice": 75000,
  "price": 100000,
  "weight": 2500,
  "capacity": 1500,
  "note": "This machine requires special training to operate.",
  "active": true,
  "buildYear": 2019,
  "emissionClass": null,
  "hourMeter": 500,
  "serviceDate": "2023-04-15T10:30:00.000Z",
  "serialNumber": "SERIAL001",
  "engineNumber": null,
  "registrationNumber": null,
  "responsibleId": "EMP001",
  "responsibleEmployeeNumber": "E001",
  "isEquipment": true
}'
```

This endpoint creates a machine.

### HTTP Request
`POST api/v4/integration/machines`



## Create Machine(s)
```shell
curl 
-X POST "http://example.com/api/v4/integration/machines/create/array" \
-H "accept: text/plain" \
-H "Content-Type: application/json" \
-d '[
      {
        "companyId": "991123",
        "id": "9911231",
        "machineNumber": "9911231",
        "department": "Manufacturing",
        "name": "High-Performance Milling Machine",
        "typeId": "MILL001",
        "costPriceMachine": 50000,
        "costPrice": 75000,
        "price": 100000,
        "weight": 2500,
        "capacity": 1500,
        "note": "This machine requires special training to operate.",
        "active": true,
        "buildYear": 2019,
        "emissionClass": null,
        "hourMeter": 500,
        "serviceDate": "2023-04-15T10:30:00.000Z",
        "serialNumber": "SERIAL001",
        "engineNumber": null,
        "registrationNumber": null,
        "responsibleId": "EMP001",
        "responsibleEmployeeNumber": "E001",
        "isEquipment": true
      }
    ]'
```

This endpoint creates a machine.

### HTTP Request
`POST api/v4/integration/machines/create/array`



## Retrieve Machine
```shell
curl 
-X GET "/api/v4/integration/machines/9911231" \
-H  "accept: text/plain" 
```
> The above command returns JSON structured like this:

```json
{
  "companyId": "991123",
  "id": "9911231",
  "machineNumber": "9911231",
  "department": "Manufacturing",
  "name": "High-Performance Milling Machine",
  "typeId": "MILL001",
  "costPriceMachine": 50000,
  "costPrice": 75000,
  "price": 100000,
  "weight": 2500,
  "capacity": 1500,
  "note": "This machine requires special training to operate.",
  "active": true,
  "buildYear": 2019,
  "emissionClass": null,
  "hourMeter": 500,
  "serviceDate": "2023-04-15T10:30:00.000Z",
  "serialNumber": "SERIAL001",
  "engineNumber": null,
  "registrationNumber": null,
  "responsibleId": "EMP001",
  "responsibleEmployeeNumber": "E001",
  "isEquipment": true
}
```

This endpoint retrieves a machine.

### HTTP Request
`GET /api/v4/integration/machines/{id}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of machine inside Ditio.



## Update Machine
```shell
curl -X PUT "/api/v4/integration/machines/991123" \
-H  "accept: text/plain" \
-H "Content-Type: application/json" \
-d '{
  "companyId": "991123",
  "id": "9911231",
  "machineNumber": "9911231",
  "department": "Data Science",
  "name": "High-Performance Drone Drill",
  "typeId": "MILL001",
  "costPriceMachine": 10,
  "costPrice": 100,
  "price": 999,
  "weight": 65,
  "capacity": 1500,
  "note": "This machine requires special training to operate.",
  "active": true,
  "buildYear": 2019,
  "emissionClass": null,
  "hourMeter": 500,
  "serviceDate": "2023-04-15T10:30:00.000Z",
  "serialNumber": "SERIAL001",
  "engineNumber": null,
  "registrationNumber": null,
  "responsibleId": "EMP001",
  "responsibleEmployeeNumber": "E001",
  "isEquipment": true
}'
```

> The above command returns the updated JSON.

This endpoint creates a machine.

### HTTP Request
`PUT /api/v4/integration/machines/{id}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of machine inside Ditio.



## Update Machine(s)

```shell
curl 
-X PUT "/api/v4/integration/machines/update/array" \
-H  "accept: text/plain" \
-H "Content-Type: application/json" \
-d '
[
  {
    "companyId": "991123",
    "id": "9911231",
    "machineNumber": "9911231",
    "department": "Data Science",
    "name": "High-Performance Drone Drill",
    "typeId": "MILL001",
    "costPriceMachine": 10,
    "costPrice": 100,
    "price": 999,
    "weight": 65,
    "capacity": 1500,
    "note": "This machine requires special training to operate.",
    "active": true,
    "buildYear": 2019,
    "emissionClass": null,
    "hourMeter": 500,
    "serviceDate": "2023-04-15T10:30:00.000Z",
    "serialNumber": "SERIAL001",
    "engineNumber": null,
    "registrationNumber": null,
    "responsibleId": "EMP001",
    "responsibleEmployeeNumber": "E001",
    "isEquipment": true
  }
]'
```

This endpoint updates the machine(s).

### HTTP Request
`POST /api/v4/integration/machines/update/array`



## Delete Machine
```shell
curl 
-X DELETE "http://example.com/api/v4/integration/machines/342342" 
-H  "accept: */*"
```

This endpoint deletes the machine.

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of machine inside Ditio.

### HTTP Request
`DELETE api/v4/integration/machines/{id}`



## Get All Machines
```shell
curl -X GET "http://example.com/api/v4/integration/machines" \
-H  "accept: text/plain"
```

> The above command returns JSON structured like this:

```json
[
  {
    "companyId": "991123",
    "id": "9911231",
    "machineNumber": "9911231",
    "department": "Manufacturing",
    "name": "High-Performance Milling Machine",
    "typeId": "MILL001",
    "costPriceMachine": 50000,
    "costPrice": 75000,
    "price": 100000,
    "weight": 2500,
    "capacity": 1500,
    "note": "This machine requires special training to operate.",
    "active": true,
    "buildYear": 2019,
    "emissionClass": null,
    "hourMeter": 500,
    "serviceDate": "2023-04-15T10:30:00.000Z",
    "serialNumber": "SERIAL001",
    "engineNumber": null,
    "registrationNumber": null,
    "responsibleId": "EMP001",
    "responsibleEmployeeNumber": "E001",
    "isEquipment": true
  }
]
```

This endpoint retrieves all the machines.

### HTTP Request
`GET /api/v4/integration/machines`


## Get Machine By Number
```shell
curl -X GET "http://example.com/api/v4/integration/machines/by-machine-number/{machineNumber}" \
-H  "accept: text/plain"
```

> The above command returns JSON structured like this:

```json
[
  {
    "companyId": "991123",
    "id": "9911231",
    "machineNumber": "9911231",
    "department": "Manufacturing",
    "name": "High-Performance Milling Machine",
    "typeId": "MILL001",
    "costPriceMachine": 50000,
    "costPrice": 75000,
    "price": 100000,
    "weight": 2500,
    "capacity": 1500,
    "note": "This machine requires special training to operate.",
    "active": true,
    "buildYear": 2019,
    "emissionClass": null,
    "hourMeter": 500,
    "serviceDate": "2023-04-15T10:30:00.000Z",
    "serialNumber": "SERIAL001",
    "engineNumber": null,
    "registrationNumber": null,
    "responsibleId": "EMP001",
    "responsibleEmployeeNumber": "E001",
    "isEquipment": true
  }
]

```

This endpoint get a machine by the machine number.

### HTTP Request
`GET /api/v4/integration/machines/by-machine-number/{machineNumber}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
machineNumber | string | External Machine Number.



## Check Can Delete Machine
```shell
curl 
-X GET "http://example.com/api/v4/integration/machines/is-machine-deletable/243234" \
-H  "accept: text/plain"
```

> The above command returns bool like this:
true

This endpoint checks whether the machine is deletable.

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of machine inside Ditio.

### HTTP Request
`GET api/v4/integration/machines/is-machine-deletable/{id}`
