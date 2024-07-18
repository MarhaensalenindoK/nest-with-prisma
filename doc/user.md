# User Api Spec

## Register User

Endpoint: POST /api/users

Request Body:

```json
{
  "username": "marhaensa",
  "password": "password",
  "name": "Marhaensalenindo Komara"
}
```

Response body (success):

```json
{
  "data": {
    "username": "marhaensa",
    "name": "Marhaensalenindo Komara"
  }
}
```

Response body (failed):

```json
{
  "errors": "..."
}
```

## Login User

Endpoint: POST /api/users/login

Request Body:

```json
{
  "username": "marhaensa",
  "password": "password"
}
```

Response body (success):

```json
{
  "data": {
    "username": "marhaensa",
    "name": "Marhaensalenindo Komara",
    "token": "...session_id_generated"
  }
}
```

Response body (failed):

```json
{
  "errors": "..."
}
```

## Get User

Endpoint: GET /api/users/current

Header:

- authorization: session_id_generated

Response body (success):

```json
{
  "data": {
    "username": "marhaensa",
    "name": "Marhaensalenindo Komara"
  }
}
```

Response body (failed):

```json
{
  "errors": "..."
}
```

## Update User

Endpoint: PATCH /api/users/current

Header:

- authorization: session_id_generated

Request Body:

```json
{
  "password": "password", // optional
  "name": "Marhaensalenindo Komara" // optional
}
```

Response body (success):

```json
{
  "data": {
    "username": "marhaensa",
    "name": "Marhaensalenindo Komara"
  }
}
```

Response body (failed):

```json
{
  "errors": "..."
}
```

## Logout User

Endpoint: DELETE /api/users/current

Header:

- authorization: session_id_generated

Response body (success):

```json
{
  "data": true
}
```

Response body (failed):

```json
{
  "errors": "..."
}
```
