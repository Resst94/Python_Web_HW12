# Task

- Implement an authentication mechanism in the application;
- implement an authorization mechanism using JWT tokens so that all operations with - contacts are performed only by registered users;
- the user has access only to his own operations with contacts;

## General requirements

-During registration, if the user already exists with this email, the server will return an HTTP 409 Conflict error;

- The server hashes the password and does not store it in the database in clear text;
- In case of successful user registration, the server should return the HTTP response status 201 Created and the new user's data;
- For all POST operations of creating a new resource, the server returns the status 201 Created;
- For the POST operation - user authentication, the server accepts a request with user data (email, password) in the request body;
- If the user does not exist or the password does not match, the HTTP 401 Unauthorized error is returned;
- the authorization mechanism using JWT tokens is implemented by a pair of tokens: access_token and refresh_token.
