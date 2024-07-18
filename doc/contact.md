# Contact API Spec

# Create Contact

Endpoint : **POST api/contacts**

Headers:

- Authorization : token

Request Body :

```json
{
  "first_name": "Marhaensalenindo",
  "last_name": "Komara",
  "email": "marhaensa@gmail.com",
  "phone": "089989898989"
}
```

Response Body :

```json
{
  "data": {
    "id": 1,
    "first_name": "Marhaensalenindo",
    "last_name": "Komara",
    "email": "marhaensa@gmail.com",
    "phone": "089989898989"
  }
}
```

# Get Contact

Endpoint : **GET api/contacts/::contactId**

Headers:

- Authorization : token

Response Body :

```json
{
  "data": {
    "id": 1,
    "first_name": "Marhaensalenindo",
    "last_name": "Komara",
    "email": "marhaensa@gmail.com",
    "phone": "089989898989"
  }
}
```

# Update Contact

Endpoint : **PUT api/contacts/::contactId**

Headers:

- Authorization : token

Request Body :

```json
{
  "first_name": "Marhaensalenindo",
  "last_name": "Komara",
  "email": "marhaensa@gmail.com",
  "phone": "089989898989"
}
```

Response Body :

```json
{
  "data": {
    "id": 1,
    "first_name": "Marhaensalenindo",
    "last_name": "Komara",
    "email": "marhaensa@gmail.com",
    "phone": "089989898989"
  }
}
```

# Remove Contact

Endpoint : **POST api/contacts/::contactId**

Headers:

- Authorization : token

Response Body :

```json
{
  "data": true
}
```

# Search Contact

Endpoint : **GET api/contacts**

Headers:

- Authorization : token

Query Params:

- name: string, contact first name or last name, optional
- phone: string, contact phone, optional
- email: string, contact email, optional
- page: number, default 1
- size: number, default 10

Response Body :

```json
{
  "data": [
    {
      "id": 1,
      "first_name": "Marhaensalenindo",
      "last_name": "Komara",
      "email": "marhaensa@gmail.com",
      "phone": "089989898989"
    }
    {....},
    {....}
  ],
  "paging": {
    "current_page": 1,
    "total_page": 10,
    "size":10,
  }
}
```
