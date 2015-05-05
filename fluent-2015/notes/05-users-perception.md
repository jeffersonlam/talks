# How Users Perceive the Speed of The Web
[Paul Irish](http://www.paulirish.com/) (Google Chrome)  
[Slides](https://docs.google.com/presentation/d/1AwT2vVHzzlsIxEUS-z769awGa-hiHTwR0iWrkeX49Fk/edit?pli=1#slide=id.g6f0232e78_056)  
[Video](https://www.youtube.com/watch?v=2ksXo2_Lfl0)  
[Fluent details page](http://fluentconf.com/javascript-html-2015/public/schedule/detail/40733)  
## Notes
What does the word "slow" mean?  
  It's a really context-sensitive word.  

> ~~What is slow?~~ What does the user feel?

Jakob Nielsen's research  
* Response times and user's perception: 100ms, 1000ms, 10ms
  * 100ms response feels immediate
  * Any longer and it feels like there's a disconnect
  * 1000ms keeps user's flow of though seamless. There's a "natural progression between tasks"
  * Beyond 1000ms, the user loses focus and attention
  * Beyond 10 seconds, you've lost the user's attention

RAIL Performance model
* Response
* Animation
* Idle
* Load

Goal response times required for user-perceived immediate feedback:  
* Tap/click: 100ms
* Drag: 16ms
* Animation: 16ms per frame (60fps)
* Page load: 1000ms
* Use idle time to proactively schedule work in 50ms chunks

Use Chrome dev tools timeline/record functionality to monitor page load times

## Action Items
* [ ] For touch-to-paint, shoot for < 100ms
* [ ] For anything animated (animations, scrolling), shoot for < 16ms per frame
* [ ] For page load, shoot for < 1000ms
* [ ] Utilize Chrome dev tools to monitor performance
