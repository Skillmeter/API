Test
====

A test represent the test entity created on Skillmeter. 

* [List Tests](#list-tests)
* [Fetch a Test](#fetch-a-test)

### List Tests

  GET /test

#### Response

Status: 200 OK

```json
[
        ...,
        {
		  "TestId": 1,
		  "Name": "Test 1",
		  "Timed": true,
		  "Duration": 20,
		  "Scored": false,
		  "Pass_Score": null,
		  "AllowSkip": true,
		  "AllowReview": true,
		  "PublicUrl": null		
        },
        ...
    ]
```


### Fetch a Test

  GET /test/:id

#### Response

  Status: 200 OK

```json
{
      "TestId": 2,
      "Name": "testé",
      "Timed": true,
      "Duration": 20,
      "Scored": false,
      "Pass_Score": null,
      "AllowSkip": true,
      "AllowReview": true,
      "PublicUrl": null
}
```
