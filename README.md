# Project MicroService {color:#003366}

This project is a simple skeleton code for microservice architecture pattern using nodejs , postgres , prisma , Rest , GraphQL.

![image!](archi.png)


# <span style="color:#003366">Technologies</span>
gRPC: Used for efficient communication between microservices.


GraphQL: Implemented for flexible and efficient querying of data.


REST: RESTful APIs are used for exposing the services to external clients.


# <span style="color:#003366">USER MICROSERVICE</span>

Contains API related to creating A new USER and API end point to get this USER

Rest :


```http
  GET /users

```
GraphQL :


```graphql
query {
   users {
    id
    name
    prenom
  }
}
```

Rest :


```http
  POST /user
```

| Parameter   | Type     | Description                       |
| :-----------| :------- | :-------------------------------- |
| `name`      | `string` | **Required**.                     |
| `prenom`    | `string` | **Required**.                     |

GraphQL :

```graphql
mutation Mutation($name: String!, $prenom: String!) {
  createUser(name: $name, prenom: $prenom) {
    id
    name
    prenom
  }
}

variable 
{
  "name": "test",
  "prenom": "test"
}

```

# <span style="color:#003366">ORDER MICROSERVICE</span>

Contains API related to creating A new ORDER and API end point to get this ORDER


Rest :


```http
  GET /orders
```

GraphQL :


```graphql
query {
   orders {
    id
    name
    description
  }
}
```
Rest :


```http
  POST /orders
```

| Parameter        | Type     | Description                       |
| :----------------| :------- | :-------------------------------- |
| `name`           | `string` | **Required**.                     |
| `description`    | `string` | **Required**.                     |


GraphQL :


```graphql
mutation Mutation($name: String!, $description: String!) {
  createOrder(name: $name, description: $description) {
    id
    name
    description
  }
}

}

variable 
{
  "name": "test",
  "description": "test"
}
```

# <span style="color:#003366">Requirements</span>

Ensure you have the following software installed on your local machine:

git

Node.js (version 12 or higher)

npm (version 6 or higher)

postgres

# <span style="color:#003366">Common setup</span>

Clone the repo and install the dependencies.

git clone https://github.com/rimbergaoui/Project.git

`cd Project`

`npm install`

# <span style="color:#003366">Run</span>

To start the ApiGateway server, run the following

`node apiGerway.js`

To start the User server, run the following

`cd userMicroservice`

`node userMicroservice.js`

To start the Order server, run the following

`cd orderMicroservice`

`node orderMicroservice.js`
