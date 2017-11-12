
# API Reference


# Get Health of node.
	  ```shell
	  curl -X GET 'http://localhost:8080/status'
	  ```
	  ```javascript
	  const request = require('request');
	  request(
	      'http://localhost:8080/status', 
	      { json: true }, 
	      (err, res, body) => {
	        console.log(body.explanation);
	      }
	  );
	  ```
	Get application health information.

### HTTP Request
  `GET http://localhost:8080/status`


# Get Service Info.
  ```shell
  curl -X GET 'http://localhost:8080/info'
  ```
  ```javascript
  const request = require('request');
  request(
      'http://localhost:8080/info', 
      { json: true }, 
      (err, res, body) => {
        console.log(body.explanation);
      }
  );
  ```

  Gets Service Info object.

### HTTP Request
  `GET http://localhost:8080/info`


# Create Service Contract
  ```shell
  curl -X POST 'http://localhost:8080/contracts'
  ```

  ```javascript
  const request = require('request');
  request(
      'http://localhost:8080/contracts', 
      { json: true }, 
      (err, res, body) => {
        console.log(body.explanation);
      }
  );
  ```
Creates a new service contract.

### Parameters

  Parameter       | In      | Type    | Required      | Description             
  --------------- | ----    | ------- | ----          | ----------------------- 
  ContractRequest | body    | string  | correlationId | The request to create a new contract.

### Schema

  Properties      | Type    | Description             
  --------------- | ------- | ----------------------- 
  correlationId   | string  | Requestor generated globally unique identifier for correleating requests.
  arguments 	  | array   |


### HTTP Request
  `POST http://localhost:8080/subscriptions/{id}/unsubscribes`



# Get Service Contract.
  ```shell
  curl -X POST 'http://localhost:8080/contracts/{id}'
  ```
  ```javascript
  const request = require('request');
  request(
      'http://localhost:8080/contracts/{id}', 
      { json: true }, 
      (err, res, body) => {
        console.log(body.explanation);
      }
  );
  ```
  Gets service contract info for a contract.

  ### Parameters

  Parameter       | In      | Type    | Required      | Description             
  --------------- | ----    | ------- | ----          | ----------------------- 
  id              | path    | string  | true          | Contract identifier.