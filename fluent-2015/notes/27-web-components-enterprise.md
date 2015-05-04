# Why Web Components are Right for Enterprise Web App Development
Benjamin Donohue (MediaMath)
3:00pm–3:30pm Wednesday, 04/22/2015

## Notes
*Screenshot of an app: 'Terminal 1'*  
There are at least 20 devs working on this one page alone.  

##### The Problem
> "We started getting a lot of redundancies, and special-snowflake styles, and whack-a-mole touch this one thing here, something else pops up there."
> "We're an enterprise business, we need to make money."

##### The Solution
Web components!  
Web components enable:  
* Stability
    * Encapsulation & Reusability
* Consistency
    * We built a style-guide.
* Velocity
    * People know exactly what modules are and how they behave.
This also benefits our partner clients: other people build on our UI.  

##### Reality Check
> "There isn't a lot of native support for web components."
Only Chrome and Opera support it. Firefox doesn't. 

##### What can we do?
Use Polyfills.

75% of our users use Chrome. Excellent!  
Other 25%, without native WC browsers: totally fine, thanks to polyfills.  
But we do disclaim...  
```
if (nonmodern) {
  obj.warning = "T1 performs best in a browser that supports Web Components. We recommend using Chrome for optimal experience."
}
```

##### STRAND
http://mediamath.github.io/strand/

## Action Items
* [ ] Use polyfills to enable web components
* [ ] Visit http://mediamath.github.io/strand/
* [ ] Visit Sid Lee Dashboard to see an example of web components in use http://dashboard.sidlee.com/
