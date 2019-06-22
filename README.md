# Python web server using Flask and GraphQL
This is an example webb app using GraphQL with Flask.

## Testing GraphQL
Go to http://localhost:5000/graphql to try GraphQL. Below are the example queries for adding a new user, getting all users, searching for a user with username and updating username with email id.
### Adding a New User
```
mutation {
  createUser(name: "abc", email: "hello@abc.com", username: "abc") {
    user {
      id,
      name,
      email,
      username
    }
    ok
  }
}
```
### Getting All Users List
```
{
  allUsers {
    edges {
      node {
        name,
        email,
        username
      }
    }
  }
}
```
### Finding a User with Username
```
{
  findUser(username: "user123") {
    id,
    name,
    email
  }
}
```
### Updating Username With Email ID
```
mutation {
  changeUsername(email: "user@example.com", username:"newuser456") {
    user {
      name,
      email,
      username
    }
  }
}
```
