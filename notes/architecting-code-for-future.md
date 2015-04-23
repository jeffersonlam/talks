# Designing for the Future: Architecting Code and Systems with Long-Term Growth and Development in Mind
Brian Belhumeur (craigslist)
@JSArtisan
5:15pm–5:45pm Wednesday, 04/22/2015
Slides: http://brianbelhumeur.github.io/Fluent2015-DesigningForTheFuture.pdf

## Notes
> "I work at Craigslist as a Front-End Developer. Now I know what you're thinking... FED at Craigslist? What the hell do you do?"
> "We need to meet the user's needs. That sounds obvious, but it's ..."
> "Craig, stop crewing with the format! You idiots can't leave well enough alone?" - CL User
> "Technical debt: Previous work that needs to be redone to continue being able to build on top of it."

##### Program with the programmer in mind
Write durable code (code that's readable and reusable into the future).
* Comments should explain the purpose of your code.
    * One line generic comment: useless. Multi-line detailed comment: useful.
* Clarity > Tiny bit of efficiency
    * Write your code to be readable, not to trim down characters.
* Weed the garden
* Red diffs
    * Red diffs (line deletions) can be a lot better than green diffs (line additions).

##### Modularity is a MUST
* Adaptability
* Optimized loading
* Isomorphism
* Testing

Quasi-Modularity

##### Computers are smart. Let machines do what they do best
* Use a build system (task-runner)
    * Gulp, Grunt, Tree Js (?)
* Use templates
    * Handlebars, EJS, Jade

##### Test "wings". You need just the right size and shape to fly.
if (probability of bug x cost of bug > ) { writeTest(); }

##### Growth and Scaling
* Caching
* Project growth curve and upgrade 12-18 months out
* Think globally and massive
* Unicode

Some things that vary internationally...
* Dollar signs
* Decimal notation
* 12 vs 24 hour clock
* Time zone
* Days of work week
...

If all goes well...
* Expanding audience
* Product scope expands
* Keep high quality users, drop low quality users
    * You don't have to please everybody. Just be sure to keep happy the users you want to keep.
* Build your tools!

##### Improving user experience
* Faster is **always** better.
    * read Browser Networking from O'Reilly
* Performance has to be built into your development process. It's not a job for cops or janitors to go in and clean up after your work.

Iterative development
1. Make it work (prototype)
2. Make it work right (debug)
3. 

Users want it...
* Easier
    * There's no such thing as too easy. The easier, the better
    * Example: Uber. Go from wanting a ride to sitting in a car on the way to destination in 3 taps. And it takes no cognitive resource.
* More efficient
    * Starbucks has their own lingo. They get users exactly what they want, efficiently.
* Better?
    * It's not user's jobs to tell you want they want to improve your site. It's your job to create something that people can easily understand and use.

What are users actually doing with your product? Find out by...
* Log parsing
* Analytics
* Real User Measurement
* Social media feedback
* Direct feedback

User's expectations change over time
* Googlization: Users have been trained to not provide context
* Sharing via all manner of social network
    * > "Your user's gonna share their experience, no matter how big or small."

> "The more familiar people are with your site, the more tunnel vision they will have using it."

## Action Items
* [ ] Read "Design of Everyday Things" by Don Norman
* [ ] Include useful comments in your code
* [ ] Keep your code modular
* [ ] Develop a development toolkit
