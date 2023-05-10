# User Certificates 

## The UserCertificate Object

> THE USERCERTIFICATE OBJECT:

```json
{
  "EmployeeNumber": "123456",
  "CertificateType": "Byggekort",
  "CertificateNumber": "78901234",
  "IssuedDateTime": "2023-05-09T10:30:00Z",
  "ValidUntilDateTime": "2024-05-09T10:30:00Z",
  "Notes": "This certificate is valid for site access."
}
```

Parameter             | Type       | Description
----------------------|------------| -----------
EmployeeNumber        | string     | This has to match the employee number in Ditio.
CertificateType       | string     | Send in a certificate type as a string. Example: Byggekort.
CertificateNumber     | string     | The unique identifier of the certificate.
IssuedDateTime        | DateTime   | The date and time when the certificate was issued.
ValidUntilDateTime    | DateTime   | The date and time until the certificate is valid.
Notes                 | string     | Additional notes for the certificate.



## Create UserCertificate
```shell
curl 
-X POST "http://example.com/api/v4/integration/certificates" \
-H "accept: text/plain" \
-H "Content-Type: application/json" \
-d '{
  "EmployeeNumber": "123456",
  "CertificateType": "Byggekort",
  "CertificateNumber": "78901234",
  "IssuedDateTime": "2023-05-09T10:30:00Z",
  "ValidUntilDateTime": "2024-05-09T10:30:00Z",
  "Notes": "This certificate is valid for site access."
}'
```

This endpoint creates a certificate for a user.

### HTTP Request
`POST api/v4/integration/certificates`