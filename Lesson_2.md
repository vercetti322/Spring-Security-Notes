# Filter Flow
Spring security in the backend is a collection of **filters** meant to control aspects of authorization/authentication (which 
can be customized) which end up at **servlet** which further connects to **spring MVC** (controller, service, etc.). An HTTP 
request enters through filter chain (by using authentication manager as entry)

## Example
The request enters the chain and passes to authentication manager which in turn uses authentication provider. Now, if the type of
auth is username/password kind, then AP uses **UserDetailService** (for user details) and **PasswordEncoder** (for hashed password)
We can make our own implementation of UserDetailService. If the authentication is successful then it goes back and stores the 
authentication object in security context.
