# Project Transactions


## Retrieve As File
```shell
curl 
-X GET "http://example.com/api/v4/project-transaction-export/file?fromWorkDate=2022-01-01&toWorkDate=2022-01-01&transactionStatus=0&userIds=123&projectIds=456&taskIds=789&machineIds=357&tagIds=457&fileName=568&lockData=true&exportDataToFileShare=true" \
-H  "accept: */*"
```

> The above command returns file.

This endpoint is used to export project transaction splits as a file. Primarily used by Ditio Web All filters are ANDed.

### HTTP Request
`GET /api/v4/project-transaction-export/file`

### Query Parameters
| Parameter | Type | Description | Required |
| --- | --- | --- | --- |
| fromWorkDate | DateTime | Export from date. Example: 2022-01-01 | Yes |
| toWorkDate | DateTime | Export to date. Example: 2022-01-23 | Yes |
| transactionStatus | Enum | Approved(0), Locked(5) or All(10). Default value is 0 (Approved) | No |
| userIds | List of string | Filter by a list of Ditio User ids | No |
| projectIds | List of string | Filter by a list of Ditio Project ids | No |
| taskIds | List of string | Filter by a list of Ditio Task ids | No |
| machineIds | List of string | Filter by a list of Ditio Machine ids | No |
| tagIds | List of string | Filter by a list of Ditio User Tag ids | No |
| fileName | string | Define a fileName In order to override the default | No |
| lockData | Boolean | Lock transaction data | No |
| exportDataToFileShare | Boolean | If data needs to be exported to the file share. Data is automatically locked if this is set to true | No |



## Retrieve As JSON
```shell
curl 
-X GET "http://example.com/api/v4/project-transaction-export?fromWorkDate=2022-01-01&toWorkDate=2022-01-23&transactionStatus=0&userIds=123,456&projectIds=789,1011&taskIds=1213,1415&machineIds=1617,1819&tagIds=2021,2223" \
-H  "accept: */*"
```

> The above command returns the JSON.

This endpoint is used this to export time registration splits as a json and all filters are ANDed.

### HTTP Request
`GET /api/v4/project-transaction-export`

### Query Parameters
| Parameter        | Type            | Description                                                                                     | Required |
|------------------|----------------|-------------------------------------------------------------------------------------------------|----------|
| fromWorkDate      | DateTime       | Export from date. Example: 2022-01-01                                                           | Yes      |
| toWorkDate        | DateTime       | Export to date. Example: 2022-01-23                                                             | Yes      |
| transactionStatus | enum           | Approved(0), Locked(5) or All(10). Default value is 0 (Approved)                                | No       |
| userIds           | List of string | Filter by a list of Ditio User ids                                                              | No       |
| projectIds        | List of string | Filter by a list  of Ditio Project ids                                                           | No       |
| taskIds           | List of string | Filter by a list  of Ditio Task ids                                                              | No       |
| machineIds        | List of string | Filter by a list  of Ditio Machine ids                                                           | No       |
| tagIds            | List of string | Filter by a list  of Ditio User Tag ids                                                          | No       |



## Lock Transactions
```shell
curl -X POST "http://example.com/api/v4/project-transaction-export/lock" \
-H "accept: */*" \
-H "Content-Type: application/json" \
-d '{
  "transactionIds": [
    "TransactionID-1",
    "TransactionID-2"
  ]
}'
```

> The above command returns the JSON.

This endpoint is used lock time registrations in Ditio.

### HTTP Request
`POST /api/v4/project-transaction-export/lock`

### Query Parameters
| Parameter       | Type            | Description                        |
|-----------------|-----------------|----------------------------------- |
| transactionIds  | List of string  | List of Ditio transaction Ids      |



## Split Transactions
```shell
curl -X GET "http://example.com/api/v4/project-transaction-export/split-transactions?fromWorkDate=2022-01-01&toWorkDate=2022-01-23&userIds=user1,user2&projectIds=project1,project2&taskIds=task1,task2&machineIds=machine1,machine2&tagIds=tag1,tag2&lockData=false" \
-H "accept: */*"
```

> The above command returns the JSON.

This endpoint is used split transactions in Ditio.

### HTTP Request
`GET /api/v4/project-transaction-export/split-transactions`

### Query Parameters
| Parameter   | Type     | Description                                          | Required |
| ----------- | -------- | ---------------------------------------------------- | -------- |
| fromWorkDate| DateTime | Export from date. Example: 2022-01-01                | Yes      |
| toWorkDate  | DateTime | Export to date. Example: 2022-01-23                  | Yes      |
| userIds     | string   | Filter by a list of Ditio User ids                   | No       |
| projectIds  | string   | Filter by a list of Ditio Project ids (default=null) | No       |
| taskIds     | string   | Filter by a list of Ditio Task ids (default=null)    | No       |
| machineIds  | string   | Filter by a list of Ditio Machine ids (default=null) | No       |
| tagIds      | string   | Filter by a list of Ditio User Tag ids (default=null)| No       |
| lockData    | bool     | Lock payroll data in Ditio (default=false)           | No       |



## Shift Report
```shell
curl -X GET "http://example.com/api/v4/project-transaction-export/shift-report?fromWorkDate=2022-01-01&toWorkDate=2022-01-23&userIds=user1,user2" \
-H "accept: */*"
```

> The above command returns the JSON.

This endpoint is used lock time registrations in Ditio.

### HTTP Request
`GET /api/v4/project-transaction-export/shift-report`

### Query Parameters
| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| fromWorkDate | string | Yes | Start date for the export. |
| toWorkDate | string | Yes | End date for the export. |
| userIds | string | Yes | Comma separated list of user IDs to filter by. |
