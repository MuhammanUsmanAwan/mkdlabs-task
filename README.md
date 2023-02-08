# Task

All this task must be done in 1 day

- in src/utils/MkdSDK.jsx implement Line 17
- in src/utils/MkdSDK.jsx implement Line 91
- in src/pages/AdminLoginPage.jsx implement Line 30
- in src/authContext.jsx implement 16

## Login

```
https://reacttask.mkdlabs.com/v2/api/lambda/login
Method POST
content-type application/json
x-project cmVhY3R0YXNrOmQ5aGVkeWN5djZwN3p3OHhpMzR0OWJtdHNqc2lneTV0Nw==
body
{
  "email": "adminreacttask@manaknight.com",
  "password": "a123456",
  "role": "admin"
}
Response
{
    "error": false,
    "role": "admin",
    "token": "",
    "expire_at": 3600,
    "user_id": 1
}
```

## Check

```
Check if token still valid
https://reacttask.mkdlabs.com/v2/api/lambda/check
Method POST
Header
x-project cmVhY3R0YXNrOmQ5aGVkeWN5djZwN3p3OHhpMzR0OWJtdHNqc2lneTV0Nw==
Bearer <token>
body
{
  "role": "admin"
}
Response
http code 200
```

## Video Paginate

```
https://reacttask.mkdlabs.com/v1/api/rest/video/PAGINATE
Method POST
Header
x-project cmVhY3R0YXNrOmQ5aGVkeWN5djZwN3p3OHhpMzR0OWJtdHNqc2lneTV0Nw==
Bearer <token>
body
{
    "payload": {},
    "page": 1,
    "limit": 10
}
Response
http code 200
{
    "error": false,
    "list": [
        {
            "id": 1,
            "title": "Rune raises $100,000 for marketing through NFT butterflies sale",
            "photo": "https://picsum.photos/200/200",
            "user_id": 1,
            "username": "boss",
            "create_at": "2022-01-01",
            "update_at": "2022-01-01T04:00:00.000Z",
            "like": 10
        }
    ],
    "page": 1,
    "limit": 10,
    "total": 112,
    "num_pages": 12
}

```
