# RESTful web service

### Reference Documentation
The following websites were used as reference to produce this project:

* [Building a CRUD API](https://auth0.com/blog/spring-boot-java-tutorial-build-a-crud-api/)
* [Securing an API](https://auth0.com/blog/spring-boot-authorization-tutorial-secure-an-api-java/)
* [Demo Client Application](https://dashboard.whatabyte.app)
* [Spring Web](https://docs.spring.io/spring-boot/docs/2.7.13/reference/htmlsingle/#web)

---

### Description
Application using Spring and Java to build a feature-complete API. A single-page web app that stores the menu items in-memory. The Spring Boot API is secured to make sure everyone is able to retrieve the menu items, but only users with the /menu-admin/ role are able to Create, Update or Delete them.

## Technologies used

- Java
- Spring Boot - Spring Web
- Gradle

1. The KeyValue dependency was used to provide all the implementation details. 
2. Used Data Validation with Spring Boot to customize the error output.
3. Used a demo client application to test the API.
4. The RESTful web service includes CORS access control headers in its response. But it's restricted to enable CORS only from the [Whatabyte](https://dashboard.whatabyte.app) origin, which is the URL of the demo application.

Additionally, the API's security was increased by requiring users to have a set of permissions (defined through a role) to perform any write operation.

### Identity and Access Management (IAM) flow:

- Users will start by authenticating with a username and password managed by Auth0.
- Once authenticated, the client will receive a JWT representing an access token.
- The client will include the access token in the authorization header of every request to a secure endpoint.
- The server will validate the access token and determine if it has the right permissions, using the information within the token.

### Contributions

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

