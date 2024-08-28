# API Spec

## Register
Endpoint : POST http://localhost:3000/register

### Request
Headers :
- Content-Type: 'application/json'
Body: {email: 'string', password: 'string'}

Example:
```json
{
    "email": "samplemail@mail.com",
    "password": "password123"
}
```

### Response
status code: 201
Content-Type: 'application/json'
Body: {message: 'string', id: 'integer', email: 'string'}

Example:
```json
{
    "message": "success create user",
    "id" : 3,
    "email": "samplemail@mail.com",
    "createdAt": "timestamp",
    "updatedAt": "timestamp"
}
```

## Login
Endpoint : POST http://localhost:3000/login

### Request
Headers :
- Content-Type: 'application/json'
Body: {email: 'string', password: 'string'}

Example:
```json
{
    "email": "samplemail@mail.com",
    "password": "password123"
}
```

### Response
Status Code: 200
- Content-Type: 'application/json'
Body: { token: 'string'}

Example:
```json
{
    "token": "jwt string"
}
```



## Create New Todo
Endpoint : POST http://localhost:3000/todo

### Request
Headers :
- Content-Type: 'application/json'
- Authorization: Bearer token

Body: 
```json
{
    "task": "task1"
}
```

### Response
Status Code: 201
- Content-Type: 'application/json'
Body: 
```json
{
    "message": "success input task",
    "task": "task1"
}
```

## Get All Todo

