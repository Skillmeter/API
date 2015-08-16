Candidate
====

A candidate represent a person assigned to take one or more tests on Skillmeter. 

* [Creating a Candidate](#creating-a-candidate)
* [Fetch a Candidate](#fetch-a-candidate)
* [Deleting a Candidate](#deleting-a-candidate)


### Creating a Candidate

  POST /candidate
  
#### Input

```json
{
"First_Name":"John",
"Last_Name":"Doe",
"Email": "john-doe@domain.com",
"Language" : "en",
"ExternalId" : "123",  
"Tests": [30, 33] 
}
```

#### Response

  Status: 201 Created


### Fetch a Candidate

  GET /candidate
  
#### Response

  Status: 200 OK

```json
{
"Tests": null,
"CandidateId": 1,
"UserId": 1,
"Email": "john-doe@domain.com",
"First_Name": "John",
"Last_Name": "Doe",
"PinCode": "aqfoymwi",
"TestDate": "2014-10-12T09:58:54.483",
"TestEndDate": "2014-10-12T09:59:15.043",
"CreatedDate": "2014-10-12T00:00:00",
"Passed": true,
"Feedback": true,
"FeedbackLevel": "M",
"FeedbackText": "",
"Language": "en",
"ExternalId": "123"
}
```
  

### Deleting a Candidate

DELETE /candidate/:id

#### Response

  Status: 204 No Content
