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
Despite this, for serious http communication in php it's likely better to use something like Guzzle or one of many libraries ... 

|Rank|Library|Description|GitHub Stars|Documentation URL|
|---|---|---|---|---|
|1|Guzzle|A PHP HTTP client that makes it easy to send HTTP requests and trivial to integrate with web services.|23.8k|[https://docs.guzzlephp.org/en/stable/](https://docs.guzzlephp.org/en/stable/)|
|2|cURL|A popular library that allows you to connect and communicate to many different types of servers.|Built-in|[https://www.php.net/manual/en/book.curl.php](https://www.php.net/manual/en/book.curl.php)|
|3|Symfony HTTP Client|A component of the Symfony framework, it provides powerful tools to make HTTP requests.|2.5k|https://symfony.com/doc/current/http_client.html|
|4|Requests|A simple HTTP library written in PHP, for PHP. It provides a consistent API for sending HTTP requests.|2.1k|https://requests.ryanmccue.info/|
|5|Buzz|A lightweight PHP library for issuing HTTP requests.|1.2k|[https://github.com/kriswallsmith/Buzz](https://github.com/kriswallsmith/Buzz)|
|6|HTTPful|A simple and chainable library for making HTTP requests.|900|[http://phphttpclient.com/](http://phphttpclient.com/)|
|7|Httplug|An HTTP client abstraction for PHP to provide unified interfaces for HTTP clients.|700|[http://httplug.io/](http://httplug.io/)|
|8|Zend Diactoros|A PSR-7 HTTP message implementation by Zend Framework, used to create and manipulate HTTP messages.|600|https://docs.zendframework.com/zend-diactoros/|
|9|Unirest|Simplifies making HTTP REST requests, even simpler than cURL.|500|http://unirest.io/php.html|
|10|ReactPHP HTTP|An async library for HTTP requests with ReactPHP.|400|https://reactphp.org/http/|


