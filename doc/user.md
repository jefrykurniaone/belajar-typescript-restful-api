# User API Spec

## Register User

Endpoint : POST /api/users

Request Body :

```json
{
    "username": "username",
    "password": "password",
    "name": "Jefry Kurniawan"
}
```

Response Body (Success) :

```json
{
    "data": {
        "username": "username",
        "name": "Jefry Kurniawan"
    }
}
```

Response Body (Failed) :

```json
{
    "errors": "Username must not blank, ..."
}
```

## Login User

Endpoint : POST /api/users/login

Request Body :

```json
{
    "username": "username",
    "password": "password"
}
```

Response Body (Success) :

```json
{
    "data": {
        "username": "username",
        "name": "Jefry Kurniawan",
        "token": "uuid"
    }
}
```

Response Body (Failed) :

```json
{
    "errors": "Username or password wrong, ..."
}
```

## Get User

Endpoint : GET /api/users/current

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
    "data": {
        "username": "username",
        "name": "Jefry Kurniawan"
    }
}
```

Response Body (Failed) :

```json
{
    "errors": "Unauthorized, ..."
}
```

## Update User

Endpoint : PATCH /api/users/current

Request Header :

- X-API-TOKEN : token

Request Body :

```json
{
    "password": "password", // optional
    "name": "Jefry Kurniawwan" // optional
}
```

Response Body (Success) :

```json
{
    "data": {
        "username": "username",
        "name": "Jefry Kurniawan"
    }
}
```

Response Body (Failed) :

```json
{
    "errors": "Unauthorized, ..."
}
```

## Logout User

Endpoint : DELETE /api/users/current

Request Header :

- X-API-TOKEN : token

Response Body (Success) :

```json
{
    "data": "OK"
}
```

Response Body (Failed) :

```json
{
    "errors": "Unauthorized, ..."
}
```
