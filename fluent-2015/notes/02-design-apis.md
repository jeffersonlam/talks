# Designing a beautiful REST API
[Les Hazlewood (Stormpath)](https://stormpath.com/)  
[Details](http://fluentconf.com/javascript-html-2015/public/schedule/detail/39033)  
[Slides](http://cdn.oreillystatic.com/en/assets/1/event/125/Designing%20a%20Beautiful%20REST+JSON%20API%20Presentation.pdf)  

A crash course on API design standards, and how to create an API that's easy to understand and use.  

## Notes
REST is Hard! (for providers)

PUT request: you must include all properties when you're updating with a PUT request  
> "PUT is idempotent"

POST
* can be used for creating and updating as well

URL vs Media-Type

URL
 * https://api.stormpath.com/v1

Media-Type
* application/foo+json;application&v=2
* application/foo2+json;application

Use camelCase  
- `myArray.forEach`, not `myArray.for_each`
- `account.givenName`, not `account.given_name`

- JS in JSON = JavaScript  
- Use UTC for timestamps


## Action Items
- [ ] Follow standards when designing/architecting a REST API
