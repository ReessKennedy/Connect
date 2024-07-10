## What ⚡
Send and received info via http requests.
## Why 🤷‍♂️
- Communicate with APPs/APIs
- Something simpler than Guzzle in just one function. 
## How 📋

|HTTP Method|Description|Handling in `sendHttpRequest` Function|
|---|---|---|
|GET|Retrieves data from the server at the specified resource.|The function checks if the method is `GET` and appends any data provided as query parameters to the URL.|
|POST|Submits data to be processed to the specified resource.|If the method is `POST`, the function encodes the data as JSON and includes it in the body of the request. It also adds the `Content-Type: application/json` header if the headers are associative.|
|PUT|Updates or replaces the specified resource with the provided data.|Similar to `POST`, if the method is `PUT`, the function encodes the data as JSON and includes it in the body of the request. It adds the `Content-Type: application/json` header if the headers are associative.|
|PATCH|Applies partial modifications to the specified resource.|This method is treated similarly to `POST` and `PUT`. The function encodes the data as JSON and includes it in the body of the request, adding the `Content-Type: application/json` header if needed.|
|DELETE|Deletes the specified resource from the server.|For `DELETE` requests, the function sets the HTTP method but does not send any data in the body.|
|OPTIONS|Describes the communication options for the target resource.|The function sets the HTTP method to `OPTIONS` and handles the request without sending any data.|
|HEAD|Retrieves the headers for the specified resource, similar to `GET`, but without the response body.|The function sets the HTTP method to `HEAD` and handles the request without sending any data in the body.|

## Resources 🌐