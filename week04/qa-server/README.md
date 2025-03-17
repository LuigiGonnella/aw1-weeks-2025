# `qa-server`

The `qa-server` is the server-side app companion for HeapOverrun. It presents some APIs to perform some CRUD operations on questions and their answers.

## APIs
Hereafter, we report the designed HTTP APIs, also implemented in the project.

### __List all questions__

URL: `/questions`

HTTP Method: GET

Description: Return all questions.

Request body:
```
```

Response: `200 OK` (success) or `500 Internal Server Error` (generic error).
Return an array with all the questions

Response body: //it returns the collection of object
```
[
    {
    "Id" : 1;
    "text" : "Is JavaScript better than Python?"
    "email" : "luigi.derussis@gmail.com"
    "userId" : 1
    "date" : "2025-02-07"
    },
...
]
```

### __Get a sinle question__

URL: `/questions/<id>`

HTTP Method: GET

Description: Return the question represented by `<id>`.

Request body:
```
```

Response: `200 OK` (success) or `404 not found` (wtong id) or `500 Internal Server Error` (generic error).
Return a single question

Response body: 
```

{
"Id" : 1;
"text" : "Is JavaScript better than Python?"
"email" : "luigi.derussis@gmail.com"
"userId" : 1
"date" : "2025-02-07"
}

```