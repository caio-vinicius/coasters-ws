# Simple-API

> A simple (and my first) REST API built with Golang

## Routes

* `GET /coasters` returns list of coasters as JSON
* `GET /coasters/{id}` returns details of specific coaster as JSON
* `POST /coasters` accepts a new coaster to be added
* `POST /coasters` returns status 415 if content is not `application/json`
* `GET /admin` requires basic auth
* `GET /coasters/random` redirects (Status 302) to a random coaster

### Return

A coaster object:
```json
{
  "id": "someid",
  "name": "name of the coaster",
  "inPark": "the amusement park the ride is in",
  "manufacturer": "name of the manufacturer",
  "height": 27,
}
```

### Persistence

There is no persistence, a temporary in-mem story is used.
