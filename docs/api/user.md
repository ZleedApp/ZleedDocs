# User

### Current User

```
GET https://zleed.ga/api/v1/user/@me
```

Request Header:

```
Authoraziton: Bearer <jwtToken>
```

Response:

```json
{
  "status": 1,
  "message": "Successfully retrieved the user.",
  "messageCode": "USER_RETRIEVED",
  "data": {
    "userId": "6f83c9f4-4d1c-4c85-9875-4d63b6b661d2",
    "userName": "example",
    "userDisplayName": "example",
    "userEmail": "email@example.com",
    "userCreated": "1661680852",
    "streamingData": {
      "streamToken": "tFyNniraaZitjk47xFpGzU1ZSPD6VaJt",
      "streamTitle": "example plays Minecraft!",
      "streamGame": "minecraft",
      "streamLanguage": "en"
    },
    "followingData": [
      "6f83c9f4-4d1c-4c85-9875-4d63b6b661d2"
    ],
    "isLive": 0,
    "isAdmin": 0
  }
}
```

### Other User

```
GET https://zleed.ga/api/v1/user/:userIdOrUserName
```

Response:

```json
{
  "status": 1,
  "message": "Successfully retrieved the user.",
  "messageCode": "USER_RETRIEVED",
  "data": {
    "userId": "6f83c9f4-4d1c-4c85-9875-4d63b6b661d2",
    "userName": "example",
    "userDisplayName": "example",
    "userCreated": "1661680852",
    "streamingData": {
      "streamTitle": "example plays Minecraft!",
      "streamGame": "minecraft",
      "streamLanguage": "en"
    },
    "isLive": 0,
    "isAdmin": 0
  }
}
```