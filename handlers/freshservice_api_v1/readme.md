# Freshservice API V1
Used for requests to the Freshservice REST API V1 Service

## Info Values
**api_username**: An integration user's username that the handler will execute requests as.

**api_password**: The password for the integration user.

**api_location**: API Location (ex: https://domain.freshdesk.com/api/v2).

**enable_debug_logging**: Yes or No. Controls logging behavior. 

## Parameters
**Error Handling**:
  Select between returning an error message, or raising an exception.

**Method**:
  HTTP Method to use for the Freshservice API call being made.
  Options are:
    - GET
    - POST
    - PUT
    - PATCH
    - DELETE

**Path**: The relative API path (to the `api_location` info value) that will be called.
  This value should begin with a forward slash `/`.

**Body**: The body content (JSON) that will be sent for POST, PUT, and PATCH requests.

### Example Use
```
  'error_handling' => 'Error Message',
  'method' => 'GET',
  'path' => '/requester',
  'body' => ''
```

## Results
**Response Body**: The returned value from the Rest Call (JSON format)

**Response Code**: The http returned code from the Rest Call.

**Handler Error Message**: A message returned in the event of an error.  The handler must be configured for *Error Message*.
