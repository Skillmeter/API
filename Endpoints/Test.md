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
		  "Category": "Programming",
		  "Timed": true,
		  "Duration": 20,
		  "Scoring": 0,
		  "Pass_Score": null,
		  "AllowSkip": true,
		  "AllowReview": true,
		  "PublicUrl": null		
        },
        ...
    ]
```
All properties are pretty much self explanatory, except Scoring which can be 0 (No scoring), 1 (Completion percentageà or 2 (Assign points to each question)

### Fetch a Test

  GET /test/:id

#### Response

  Status: 200 OK

```json
{
      "TestId": 2,
      "Name": "Test 2",
      "Category": "Programming",
      "Timed": true,
      "Duration": 20,
      "Scoring": 0,
      "Pass_Score": null,
      "AllowSkip": true,
      "AllowReview": true,
      "PublicUrl": null
}
```
