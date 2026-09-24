1. POST request with probe in the body: Status Code - 201 | Devices - 6

2. POST request with probe in the body again: Status Code - 201 | Devices - 7

3. PUT request with attic body: Status Code - 200 | Devices: 7

4. PUT request with attic body again: Status Code - 200 | Devices: 7

5. DELETE /device/fridge: Status Code - 200 | Devices - 6

6. DELETE request again: Status Code - 404 | Devices - 6 


The PUT method left the system in the same state whether it was sent once or twice.
DELETE and POST will change the state of the system depending on how many times the specific request is sent.
DELETE and POST are idempotent requests.