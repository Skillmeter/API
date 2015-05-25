# Skillmeter API

## Table of Contents
* [Introduction](#introduction)
* [Authentication](#authentication)
* [Errors](#errors)
* [Endpoints](#endpoints)
	* [Test](Endpoints/Test.md)
	* [Candidate](Endpoints/Candidate.md)
* [Integration scenario - WIP] (IntegrationScenario.md)

## Introduction

Skillmeter is an online testing platform. Our HTTP API was designed to be easy to integrate into your workflow.

We have done our best to follow [REST](https://en.wikipedia.org/wiki/Representational_state_transfer) principles when designing the API. **Please note that this API is currently in beta and subject to change.** Any changes or new additions will be announced in the [changelog](CHANGELOG.md). You can also receive API-related announcements [@skillmeter](https://twitter.com/skillmeter).

### API Endpoint

    https://api.skillmeter.com

### JSON-only

All responses will be in [JSON](https://en.wikipedia.org/wiki/JSON). Input data passed through the request body can be form-encoded or JSON-encoded. If using a JSON body, please specify the `Content-Type` header as `application/json`.

### Getting Help or Contributing

Please report any issues or suggestions in the [issues](https://github.com/skillmeter/api/issues). If you need help using the API or need to discuss anything sensitive please message us at support@skillmeter.com. Any pull requests to improve this document are welcome!

## Authentication

The API uses [HTTP Basic Authentication](https://en.wikipedia.org/wiki/Basic_access_authentication) to authenticate users.  The credentials are the same as the ones on Skillmeter, with username being the email address. Also, **all requests must use HTTPS.** Any HTTP requests will be ignored.

## Errors

A 4xx or 5xx status code will be returned upon a failed request.

Possible error codes:

* `401` Unauthorized
* `403` Forbidden - correctly authenticated but missing permission to execute the request
* `404` Not Found - returned when trying to access an entity that does not exist
* `500` Internal Server Error - something has broke on our end



## Endpoints
* [Test](Endpoints/Test.md)
* [Candidate](Endpoints/Candidate.md)
