# Address API Spec

# Create address

Endpoint : **POST api/contact/::contact_id/addresses**

Headers:

- Authorization : token

Request Body :

```json
{
  "street": "jalan .........",
  "city": "Kota .........",
  "province": "Provinsi .........",
  "country": "Negara .........",
  "postal_code": "11 ........."
}
```

Response Body :

```json
{
  "data": {
    "id": 1,
    "street": "jalan .........",
    "city": "Kota .........",
    "province": "Provinsi .........",
    "country": "Negara .........",
    "postal_code": "11 ........."
  }
}
```

# Get address

Endpoint : **GET api/contact/::contact_id/addresses/::addressId**

Headers:

- Authorization : token

Response Body :

```json
{
  "data": {
    "id": 1,
    "street": "jalan .........",
    "city": "Kota .........",
    "province": "Provinsi .........",
    "country": "Negara .........",
    "postal_code": "11 ........."
  }
}
```

# Update address

Endpoint : **PUT api/contact/::contact_id/addresses/::address_id**

Headers:

- Authorization : token

Request Body :

```json
{
  "street": "jalan .........",
  "city": "Kota .........",
  "province": "Provinsi .........",
  "country": "Negara .........",
  "postal_code": "11 ........."
}
```

Response Body :

```json
{
  "data": {
    "id": 1,
    "street": "jalan .........",
    "city": "Kota .........",
    "province": "Provinsi .........",
    "country": "Negara .........",
    "postal_code": "11 ........."
  }
}
```

# Remove address

Endpoint : **DELETE api/contact/::contact_id/addresses/::address_id**

Headers:

- Authorization : token

Response Body :

```json
{
  "data": true
}
```

# List address

Endpoint : **GET api/contact/::contact_id/addresses**

Headers:

- Authorization : token

Response Body :

```json
{
  "data": [
    {
      "id": 1,
      "street": "jalan .........",
      "city": "Kota .........",
      "province": "Provinsi .........",
      "country": "Negara .........",
      "postal_code": "11 ........."
    },
    {......},
    {......},
    {......},
  ]
}
```
