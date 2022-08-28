# Auth

### Register

```
POST https://zleed.ga/api/v1/auth/register
```

Request Body:

```json
{
  "username": "example",
  "email": "email@example.com",
  "password": "examplepasswd123"
}
```

Response:

=== "Success (200)"

    ```json
    {
      "status": 1,
      "message": "Created User.",
      "messageCode": "USER_CREATED",
      "data": {
        "jwtToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1dWlkIjoiNmY4M2M5ZjQtNGQxYy00Yzg1LTk4NzUtNGQ2M2I2YjY2MWQyIiwidXNlcm5hbWUiOiJleGFtcGxlIn0.6r8bDbhQVwypwswfRbdNcwfW6k4ue_EvPiK7np_NAPA",
        "jwtExpires": "1735686000"
      }
    }
    ```

=== "Error - Username Taken (400)"

    ```json
    {
      "status": 0,
      "message": "The username is already in use.",
      "messageCode": "USERNAME_TAKEN",
      "data": null
    }
    ```

=== "Error - Email Taken (400)"

    ```json
    {
      "status": 0,
      "message": "The email is already in use.",
      "messageCode": "EMAIL_TAKEN",
      "data": null
    }
    ```

### Login

```
POST https://zleed.ga/api/v1/auth/login
```

Request Body:

```json
{
  "email": "email@example.com",
  "password": "examplepasswd123"
}
```

Response:

=== "Success (200)"

    ```json
    {
      "status": 1,
      "message": "Successfully logged in the user.",
      "messageCode": "USER_FOUND",
      "data": {
        "jwtToken": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1dWlkIjoiNmY4M2M5ZjQtNGQxYy00Yzg1LTk4NzUtNGQ2M2I2YjY2MWQyIiwidXNlcm5hbWUiOiJleGFtcGxlIn0.6r8bDbhQVwypwswfRbdNcwfW6k4ue_EvPiK7np_NAPA",
        "jwtExpires": "1735686000"
      }
    }
    ```

=== "Error - Invalid Password (400)"

    ```json
    {
      "status": 0,
      "message": "The password is invalid.",
      "messageCode": "PASSWORD_INVALID",
      "data": null
    }
    ```

=== "Error - Invalid Email (400)"

    ```json
    {
      "status": 0,
      "message": "The email is invalid.",
      "messageCode": "EMAIL_INVALID",
      "data": null
    }
    ```

### Message Codes

| **Message Code**   | **Message**                      |
|--------------------|----------------------------------|
| `USER_CREATED`     | Successfully created user.       |
| `USER_FOUND`       | Successfully logged in the user. |
| `USERNAME_TAKEN`   | The username is already in use.  |
| `EMAIL_TAKEN`      | The email is already in use.     |
| `PASSWORD_INVALID` | The password is invalid.         |
| `EMAIL_INVALID`    | The email is invalid.            |