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
"First_Name":"John" ,
"Last_Name":"Doe",
"Email": "john-doe@domain.com",
"Language" : "en",
"ExternalId" : "111",
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
  "invoice": {
    "customer": 15444,
    "name": "Monthly Paper Delivery",
    "currency": "usd",
    "estimate": null,
    "subscription": null,
    "theme": 432,
    "chase": false,
    "number": "INV-0016",
    "date": 1416290400,
    "due_date": 1416549600,
    "payment_terms": null,
    "purchase_order": null,
    "items": [
      {
        "id": 7,
        "item": 79,
        "plan": null,
        "type": "product",
        "name": "Copy Paper, Case",
        "description": "20 lb., 92 US / 104 Euro Bright, Ideal for toner-based copiers, plain-paper fax machines,and printers",
        "quantity": 1,
        "unit_cost": 45,
        "amount": 45,
        "discounts": [],
        "taxes": [],
        "shipping": []
      },
      {
        "id": 8,
        "item": 83,
        "plan": null,
        "type": "service",
        "name": "Delivery",
        "description": "",
        "quantity": 1,
        "unit_cost": 10,
        "amount": 10,
        "discounts": [],
        "taxes": [],
        "shipping": []
      }
    ],
    "terms": null,
    "notes": null,
    "subtotal": 55,
    "discounts": [],
    "taxes": [
      {
        "id": 2084,
        "amount": 3.85,
        "rate": {
          "id": 304,
          "type": "tax",
          "name": "Sales Tax",
          "number": "FI-8200",
          "is_percent": true,
          "value": 7
        }
      }
    ],
    "shipping": [],
    "total": 51.15,
    "amount_paid": 0,
    "amount_adjusted": 0,
    "balance": 51.15,
    "draft": false,
    "sent": false,
    "closed": false,
    "paid": false,
    "url": "https://dundermifflin.invoiced.com/invoices/IZmXbVOPyvfD3GPBmyd6FwXY",
    "pdf_url": "https://dundermifflin.invoiced.com/invoices/IZmXbVOPyvfD3GPBmyd6FwXY/pdf",
    "csv_url": "https://dundermifflin.invoiced.com/invoices/IZmXbVOPyvfD3GPBmyd6FwXY/csv",
    "status": "not_sent",
    "next_chase_on": null,
    "attempt_count": 0,
    "next_payment_attempt": null,
    "stripe_invoice": null,
    "disabled_payment_methods": {
      "paypal": true
    }
  }
}
```
  

### Deleting a Candidate

DELETE /candidate/:id

#### Response

  Status: 204 No Content
