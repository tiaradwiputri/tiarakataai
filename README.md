# Dependency Injection

This is a take home assignment to create a warehousing system that enables one service to handle all data management. The system will be developed in iterations. Each branch represent an iteration with third iteration as master branch.

To start the application please use command `node index.js` or `nodemon`. To start test please use command `npm run test`, please make sure the server is running before execute the test.

# First iteration
CRUD operations for conversation log and user profile. The data shall be stored in memory using Memstore module.
Access the API with the following HTTP requests
```
GET /users
GET /users/{id}
POST /users
PUT /users/{id}
DELETE /users/{id}
```

```
GET /conversations
GET /conversations/{id}
POST /conversations
PUT /conversations/{id}
DELETE /converations/{id}
```
## Questions
1. Why the type of `store` is `Store` and not `Memstore`?
2. What dessign patterns is used on the first iteration?

# Second iteration
An `Injector` acted as container to manage components defined in configuration JSON file to manage components.

## Questions
1. What is the advantage of having initialization in configuration file?
2. What is the pattern with an `Injector` called?
3. What is needed in order to swap the implementation to a `DBStore` components?
4. What steps should be done to have a definable environment variable in configuration file?

# Third iteration
A generic repository to handle generic data repository with schema definable in the configuration file.

## Questions
1. What is the benefit of the changes?
2. What should be changed to add a new data repository? i.e. path `/tokens` with the fields: `string token; int expire`
