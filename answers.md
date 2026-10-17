1. POST request with probe in the body: Status Code - 201 | Devices - 6

2. POST request with probe in the body again: Status Code - 201 | Devices - 7

3. GET request for probe bodies:  Status Code - 200 | Devices - 7

4. PUT request with attic body: Status Code - 200 | Devices: 7

5. PUT request with attic body again: Status Code - 200 | Devices: 7

6. DELETE /device/fridge: Status Code - 200 | Devices - 6

7. DELETE request again: Status Code - 404 | Devices - 6 


The PUT, GET and DELETE method left the system in the same state whether it was sent twice.
POST will change the state of the system depending on how many times the specific request or the state of the handler.  In this tutorial POST is also idempotent because you cannot POST duplicate device.
PUT, GET and DELETE are idempotent requests.  POST in this case is also idempotent but is not always.