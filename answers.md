1. POST request with probe in the body: Status Code - 201 | Devices - 6

2. POST request with probe in the body again: Status Code - 201 | Devices - 7

3. GET request for probe bodies:  Status Code - 200 | Devices - 7

4. PUT request with attic body: Status Code - 200 | Devices: 7

5. PUT request with attic body again: Status Code - 200 | Devices: 7

6. DELETE /device/fridge: Status Code - 200 | Devices - 6

7. DELETE request again: Status Code - 404 | Devices - 6 


The PUT and GET method left the system in the same state whether it was sent once or twice.
DELETE and POST will change the state of the system depending on how many times the specific request is sent.
PUT and GET are idempotent requests.