# Designing a beautiful REST API
@lhazlewood (Stormpath)  
HATEOS  
hypermedia as the engine of application state  

## Notes
Rest is Hard! (for providers)

Example Domain: Stormpath
    applications
    directories
    accounts
    groups
    associations
    workflows

Collection Resource
    /applications

PUT request: you must include all properties when you're updating with a PUT request
    "PUT is idempotent"
POST
    can be used for creating and updating as well

URL
    https://api.stormpath.com/v1
vs
Media-Type
application/foo+json;application&v=2
application/foo2+json;application

Media Type != JSON ?
camcelCase

JS in JSON = JavaScript
myArray.forEach
Not myArray.for_each

account.givenName
Not account.given_name

-use camelcase
-Use UTC for timestamps

Should you include a response body in a response?
For a GET, of course. But what about POST?

Header
    -Accept header
    -header values comma delimited
    -q param determines precedence, defaults to 1, then conventionally by list order
    GET /aplications/a1b2c3
    Accept: application/json, text/plain:q=0.8

## Action Items
