# Fundamentals
We will deal with application-level security here (as network-level and others are not handled by Spring). The two main concepts 
in application-level security are :- **Authentication** & **Authorization**.

## Authentication
When the application wants to figure out who is the user trying to access the application. It can be done in many ways like :-
using username/password, certificates, 2FA, MFA, fingerprint scanning, etc.

## Authorization
When the application has authenticated the user, it needs to authorize or assign a defined access to it in which the user can 
interact with the application. The user has certain **authority** to perform a task by acting as a **role**.

Spring security is 99% of times for web applications but it can be used for other applications also. By default, spring security
configures all end-points to be authenticated with single HTTP basic auth. (The HTTP basic auth is known as authorization but it
can do authentication as well). In the header of auth, the username and password are concatenated (by ':') and base64 **encoded**.

## Encryption vs Encoding
Encoding is a mathematical function which transforms the string to an encoding which can be reversed given that one knows abt the 
function. While in case of encryption, alongwith a function we also have a secret key which is necessary to revert back to original
string (making it more secure).
