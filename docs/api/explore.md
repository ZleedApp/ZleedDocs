# Explore

### Currently Live

```
GET https://zleed.ga/api/v1/explore/live
```

Response:

=== "Success (200)"
    ```json
    {
      "status": 1,
      "message": "Successfully retrieved live users.",
      "messageCode": "LIVE_USERS_RETRIEVED",
      "data": [
        {
          "userId": "6f83c9f4-4d1c-4c85-9875-4d63b6b661d2",
          "userName": "example",
          "userDisplayName": "example",
          "userCreated": "1661680852",
          "streamingData": {
            "streamTitle": "example plays Minecraft!",
            "streamGame": "minecraft",
            "streamLanguage": "en"
          },
          "isLive": 1,
          "isAdmin": 0
        },
        ...
      ]
    }
    ```

### All Users

```
GET https://zleed.ga/api/v1/explore/all
```

Response:

=== "Success (200)"
    ```json
    {
      "status": 1,
      "message": "Successfully retrieved all users.",
      "messageCode": "ALL_USERS_RETRIEVED",
      "data": [
        {
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
        },
        ...
      ]
    }
    ```

### Message Codes

| **Message Code**       | **Message**                        |
|------------------------|------------------------------------|
| `LIVE_USERS_RETRIEVED` | Successfully retrieved live users. |
| `ALL_USERS_RETRIEVED`  | Successfully retrieved all users.  |