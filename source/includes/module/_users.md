# Users 

## The User Object

> THE USER OBJECT:

```json
{
  "IdentityId": "123456",
  "CompanyProfileId": "7890",
  "CompanyId": "ABC123",
  "EmployeeNumber": "E1234",
  "FirstName": "John",
  "LastName": "Doe",
  "MobileWork": "555-1234",
  "MobilePrivate": "555-5678",
  "Email": "johndoe@example.com",
  "WorkTitle": "Software Developer",
  "BirthDate": "1990-05-09",
  "CarRegNumber": "AB12345",
  "EmploymentStartDate": "2015-01-01",
  "EmploymentEndDate": null,
  "Department": "IT",
  "CardId": "C123",
  "CardExpirationDate": "2025-12-31",
  "Payroll": true,
  "IsDisabled": false,
  "DefaultResourceNumber": "R123",
  "WorktimeArrangementName": "Standard",
  "OrganizationNumber": "123456789"
}
```

Parameter                 | Type     | Description
--------------------------|----------|------------
IdentityId                | string   | The identity ID of the user.
CompanyProfileId          | string   | The company profile ID of the user.
CompanyId                 | string   | The ID of the company the user belongs to.
EmployeeNumber            | string   | The employee number of the user.
FirstName                 | string   | The first name of the user.
LastName                  | string   | The last name of the user.
MobileWork                | string   | The work mobile number of the user.
MobilePrivate             | string   | The private mobile number of the user.
Email                     | string   | The email of the user.
WorkTitle                 | string   | The work title of the user.
BirthDate                 | string   | The birth date of the user.
CarRegNumber              | string   | The car registration number of the user.
EmploymentStartDate       | string   | The start date of the user's employment.
EmploymentEndDate         | string   | The end date of the user's employment.
Department                | string   | The department of the user.
CardId                    | string   | The ID of the card.
CardExpirationDate        | string   | The expiration date of the card.
Payroll                   | bool     | Indicates if the user is on payroll or not.
IsDisabled                | bool     | Indicates if the user is disabled or not.
DefaultResourceNumber     | string   | The default resource number of the user.
WorktimeArrangementName   | string   | The name of the worktime arrangement.
OrganizationNumber        | string   | The organization number of the user.



## Create User
```shell
curl 
-X POST "http://example.com/api/v4/integration/users" \
-H "accept: text/plain" \
-H "Content-Type: application/json" \
-d '{
  "IdentityId": "123456",
  "CompanyProfileId": "7890",
  "CompanyId": "ABC123",
  "EmployeeNumber": "E1234",
  "FirstName": "John",
  "LastName": "Doe",
  "MobileWork": "555-1234",
  "MobilePrivate": "555-5678",
  "Email": "johndoe@example.com",
  "WorkTitle": "Software Developer",
  "BirthDate": "1990-05-09",
  "CarRegNumber": "AB12345",
  "EmploymentStartDate": "2015-01-01",
  "EmploymentEndDate": null,
  "Department": "IT",
  "CardId": "C123",
  "CardExpirationDate": "2025-12-31",
  "Payroll": true,
  "IsDisabled": false,
  "DefaultResourceNumber": "R123",
  "WorktimeArrangementName": "Standard",
  "OrganizationNumber": "123456789"
}'
```

This endpoint creates a Task.

### HTTP Request
`POST /api/v4/integration/users`



## Retrieve User
```shell
curl 
-X GET "/api/v4/integration/users/by-profile-id/123456" \
-H  "accept: text/plain" 
```

> The above command returns JSON structured like this:

```json
{
  "IdentityId": "123456",
  "CompanyProfileId": "7890",
  "CompanyId": "ABC123",
  "EmployeeNumber": "E1234",
  "FirstName": "John",
  "LastName": "Doe",
  "MobileWork": "555-1234",
  "MobilePrivate": "555-5678",
  "Email": "johndoe@example.com",
  "WorkTitle": "Software Developer",
  "BirthDate": "1990-05-09",
  "CarRegNumber": "AB12345",
  "EmploymentStartDate": "2015-01-01",
  "EmploymentEndDate": null,
  "Department": "IT",
  "CardId": "C123",
  "CardExpirationDate": "2025-12-31",
  "Payroll": true,
  "IsDisabled": false,
  "DefaultResourceNumber": "R123",
  "WorktimeArrangementName": "Standard",
  "OrganizationNumber": "123456789"
}
```

This endpoint retrieves a user.

### HTTP Request
`GET /api/v4/integration/users/by-profile-id/{profileId}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
profileId | string | Unique identifier of a user profile inside Ditio.



## Update User
```shell
curl 
-X PUT "/api/v4/integration/users/123456" \
-H  "accept: text/plain" 
-d '{
  "IdentityId": "123456",
  "CompanyProfileId": "7890",
  "CompanyId": "ABC123",
  "EmployeeNumber": "E1234",
  "FirstName": "Johnathan",
  "LastName": "Doe",
  "MobileWork": "555-1234",
  "MobilePrivate": "555-5678",
  "Email": "johndoe@example.com",
  "WorkTitle": "Software Developer 2",
  "BirthDate": "1990-05-09",
  "CarRegNumber": "AB12345",
  "EmploymentStartDate": "2015-01-01",
  "EmploymentEndDate": null,
  "Department": "IT",
  "CardId": "C123",
  "CardExpirationDate": "2025-12-31",
  "Payroll": true,
  "IsDisabled": false,
  "DefaultResourceNumber": "R123",
  "WorktimeArrangementName": "Standard",
  "OrganizationNumber": "123456789"
}'
```

> The above command returns the updated JSON.

This endpoint updates the user information stored in Ditio. Can be an issue, if multiple Employment-related fields are updated at the same time. Note, that when the user starts working for a new company, you should provide a valid start date

### HTTP Request
`PUT /api/v4/integration/users/{identityId}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
identityId | string | Unique identifier of a user profile inside Ditio.



## Delete User
```shell
curl 
-X DELETE "http://example.com//api/v4/integration/users/123456" 
-H  "accept: */*"
```

This endpoint deletes a user.

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
id | string | Unique identifier of a Task inside Ditio.

### HTTP Request
`DELETE /api/v4/integration/users/{identityId}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
identityId | string | Unique identifier of a user profile inside Ditio.



## Get All Users
```shell
curl 
-X GET "/api/v4/integration/users" \
-H  "accept: text/plain" 
```

> The above command returns JSON structured like this:

```json
[
  {
    "IdentityId": "123456",
    "CompanyProfileId": "7890",
    "CompanyId": "ABC123",
    "EmployeeNumber": "E1234",
    "FirstName": "John",
    "LastName": "Doe",
    "MobileWork": "555-1234",
    "MobilePrivate": "555-5678",
    "Email": "johndoe@example.com",
    "WorkTitle": "Software Developer",
    "BirthDate": "1990-05-09",
    "CarRegNumber": "AB12345",
    "EmploymentStartDate": "2015-01-01",
    "EmploymentEndDate": null,
    "Department": "IT",
    "CardId": "C123",
    "CardExpirationDate": "2025-12-31",
    "Payroll": true,
    "IsDisabled": false,
    "DefaultResourceNumber": "R123",
    "WorktimeArrangementName": "Standard",
    "OrganizationNumber": "123456789"
  }
]
```

This endpoint gets the list of Users inside Current company (includes subsidiary companies) or only inside specified company.

### HTTP Request
`GET /api/v4/integration/users`



## Check Can Delete User
```shell
curl 
-X GET "/api/v4/integration/users/is-identity-deletable/123456" \
-H  "accept: text/plain" 
```

> The above command returns bool like this:
true

This endpoint checks if the user can be deleted

### HTTP Request
`GET /api/v4/integration/users/is-identity-deletable/{identityId}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
identityId | string | Unique identifier of a user profile inside Ditio.



## Get User By Employee Number
```shell
curl 
-X GET "/api/v4/integration/users/by-employee-number/E1234" \
-H  "accept: text/plain" 
```

> The above command returns JSON structured like this:

```json
{
  "IdentityId": "123456",
  "CompanyProfileId": "7890",
  "CompanyId": "ABC123",
  "EmployeeNumber": "E1234",
  "FirstName": "John",
  "LastName": "Doe",
  "MobileWork": "555-1234",
  "MobilePrivate": "555-5678",
  "Email": "johndoe@example.com",
  "WorkTitle": "Software Developer",
  "BirthDate": "1990-05-09",
  "CarRegNumber": "AB12345",
  "EmploymentStartDate": "2015-01-01",
  "EmploymentEndDate": null,
  "Department": "IT",
  "CardId": "C123",
  "CardExpirationDate": "2025-12-31",
  "Payroll": true,
  "IsDisabled": false,
  "DefaultResourceNumber": "R123",
  "WorktimeArrangementName": "Standard",
  "OrganizationNumber": "123456789"
}
```

This endpoint retrieves a user with employee number.

### HTTP Request
`GET /api/v4/integration/users/by-employee-number/{employeeNumber}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
employeeNumber | string | Employee number of a user inside a company in Ditio.



## Enable User
```shell
curl 
-X PATCH "http://example.com/api/v4/integration/users/enable/23423423" \
-H  "accept: */*"
```

> The above command returns no data.

This endpoint sets user to Enabled state.

### HTTP Request
`PATCH /api/v4/integration/users/enable/{profileId}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
profileId | string | Unique identifier of a user profile inside Ditio.



## Disable User
```shell
curl 
-X PATCH "http://example.com/api/v4/integration/users/disable/23423423" \
-H  "accept: */*"
```

> The above command returns no data.:

This endpoint sets user to Disabled state with disable reason = disabledByIntegration.

### HTTP Request
`PATCH /api/v4/integration/users/disable/{profileId}`

### Query Parameters
Parameter | Type | Description
--------- | ------- | -----------
profileId | string | Unique identifier of a user profile inside Ditio.



## Create User SCIM endpoint
```shell
curl 
-X POST "http://example.com/api/v4/integration/users/scim" \
-H "accept: text/plain" \
-H "Content-Type: application/json" \
-d '{
  "IdentityId": "123456",
  "CompanyProfileId": "7890",
  "CompanyId": "ABC123",
  "EmployeeNumber": "E1234",
  "FirstName": "John",
  "LastName": "Doe",
  "MobileWork": "555-1234",
  "MobilePrivate": "555-5678",
  "Email": "johndoe@example.com",
  "WorkTitle": "Software Developer",
  "BirthDate": "1990-05-09",
  "CarRegNumber": "AB12345",
  "EmploymentStartDate": "2015-01-01",
  "EmploymentEndDate": null,
  "Department": "IT",
  "CardId": "C123",
  "CardExpirationDate": "2025-12-31",
  "Payroll": true,
  "IsDisabled": false,
  "DefaultResourceNumber": "R123",
  "WorktimeArrangementName": "Standard",
  "OrganizationNumber": "123456789"
}'
```

This endpoint creates or updates a user from a SCIM endpoint.

### HTTP Request
`POST /api/v4/integration/users/scim`








