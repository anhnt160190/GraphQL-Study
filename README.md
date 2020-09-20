# Study GraphQL

Follow series [GraphQL](https://www.udemy.com/share/101WucB0cZcVtTRHg=/)

### Getting Started

Make sure you have NodeJS on your machine

Create db.json
```
# example for db.json
{
  "users": [
    {
      "id": "1",
      "firstName": "Samantha",
      "age": 22,
      "companyId": "1"
    }
  ],
  "companies": [
    {
      "id": "1",
      "name": "Apple",
      "description": "iphone"
    }
  ]
}
```

```bash
$ npm install -g json-server
$ json server --watch db.json
```

### Start Server
```
# dev
$ yarn dev
# production
$ yarn start
```

Now you can access & test graphQL at localhost:4000/graphql

### Example
- Create query for get users

```
{
  user(id: "1") {
    id,
    firstName,
    age,
    company {
      id,
      name
    }
  }
}
```

Your result
```
{
  "data": {
    "user": {
      "id": "1",
      "firstName": "Samantha",
      "age": 22,
      "company": {
        "id": "2",
        "name": "Google"
      }
    }
  }
}
```