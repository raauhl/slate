# Payroll Exports


## Get Payroll Data - Method 1
```shell
curl 
-X GET "https://example.com/api/payroll-export?fromWorkDate=2022-01-01&toWorkDate=2022-01-23&modifiedSinceDate=2022-01-23&dataFilter=0&userIds=123,456" \
-H  "accept: text/plain"
```

> The above command returns the JSON.

This endpoint is used to export payroll data as a json all filters are ANDed IMPORTANT: For getting data out using the "fromWorkDate" and "toWorkDate" parameters, the maximum date range supported is 30 days. For longer reports, please chunk the requests with a max. 30 day range. For getting data out using the "modifiedSinceDate" parameter, the oldest data that can be queried in this way is 1 year back since current date. If "fromWorkDate" and "toWorkDate" parameters are specified along with the "modifiedSinceDate" parameter, then data modified since that date is queried inside the specified range

### HTTP Request
`GET api/payroll-export/readonly`

### Query Parameters
| Parameter         | Type             | Description                                                                                       | Required |
|-------------------|------------------|---------------------------------------------------------------------------------------------------|----------|
| fromWorkDate      | DateTime?       | Export from date. Example: 2022-01-01                                                             | No       |
| toWorkDate        | DateTime?       | Export to date. Example: 2022-01-23                                                               | No       |
| modifiedSinceDate | DateTime?       | Returns all payroll data that has been modified since the given date. Example: 2022-01-23         | No       |
| dataFilter        | enum            | Approved(0), Locked(5) or All(10). Default value is 0 (Approved)                                 | No       |
| userIds           | List of string | Filter by a list of Ditio User ids                                                                | No       |




## Get Payroll Data - Method 2
```shell
curl 
-X GET "http://example.com/api/payroll-export?fromWorkDate=2022-01-01&toWorkDate=2022-01-23&lockData=false&dataFilter=0&userIds=123,456,789" \
-H  "accept: text/plain"
```

> The above command returns the JSON.

This endpoint is used to export payroll data as a json. Includes possibility to lock payroll data. All filters are ANDed and IMPORTANT: Maximum date range supported is 30 days. For longer reports, please chunk the requests with a max of 30 day range.
        
### HTTP Request
`GET /api/payroll-export`

### Query Parameters
| Parameter    | Type             | Description                                                           | Required |
|--------------|------------------|-----------------------------------------------------------------------|----------|
| fromWorkDate | DateTime         | Export from date. Example: 2022-01-01                                 | Yes      |
| toWorkDate   | DateTime         | Export to date. Example: 2022-01-23                                   | Yes      |
| lockData     | Boolean          | Lock payroll data in Ditio                                            | No       |
| dataFilter   | enum             | Approved(0), Locked(5) or All(10). Default value is 0 (Approved)     | No       |
| userIds      | List of string  | Filter by a list of Ditio User ids                                    | No       |



## Get Payroll Data as File
```shell
curl 
-X GET "http://example.com/api/payroll-export/file?fromWorkDate=2022-01-01&toWorkDate=2022-01-23&voucherNumber=123&dataExportType=6&dataFilter=0" \
-H  "accept: text/plain"
```

> The above command returns a file.

This endpoint gets Payroll data out as a file in the specific format set up in the Company Payroll Setup IMPORTANT: Maximum date range supported is 30 days. For longer reports, please chunk the requests with a max. 30 day range

### HTTP Request
`GET /api/payroll-export/file`

### Query Parameters
| Parameter     | Type     | Description                                                                                   | Required |
|---------------|----------|-----------------------------------------------------------------------------------------------|----------|
| fromWorkDate  | DateTime | Export from date. Example: 2022-01-01                                                         | Yes      |
| toWorkDate    | DateTime | Export to date. Example: 2022-01-23                                                           | Yes      |
| voucherNumber | string   | Voucher number for cost file export                                                           | No       |
| dataExportType| enum     | Payroll Preview file export(5), Payroll Journal export(6), Payroll file export(10), Absence file Export(20), Cost file export(30), Transaction split export(40). Default Value is 6 (Payroll Journal export) | No       |
| dataFilter    | enum     | Approved(0), Locked(5) or All(10). Default value is 0 (Approved)                             | No       |
