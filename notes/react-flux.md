# React and Flux: Two Great Tastes that Taste Great Together
Bill Fisher (Facebook)  
11:15am–11:45am Tuesday, 04/21/2015  
Presentation: https://speakerdeck.com/fisherwebdev/fluent-react-flux

---

"Mental models matter a lot. If you can't draw a diagram of how your app works in about 5 seconds..."

## Flux
Structure:  
[Actions] - [Dispatcher] - [Store] - [View]

##### Actions
past-tense in method and property  

##### Dispatcher
broadcasting the status throughout the entire application  
available through npm or bower as flux  

##### Store
"A lot of where the meat of the flux application lives."  
each store is a singleton  
manage state for a logical domain  
Callback is the only way data gets into the store  
No setters, only getters: a universe unto itself  
Emits an event when state has changed  

##### Views
Views & "Controller" views  

### React

##### React & the DOM
On the web, we use the virtual DOM. It basically keeps track of the state of the DOM.  
We diff between the two, and come up with the ideal way to update DOM in one fell swoop.  
We can stop think about managing the DOM.  

##### React's Paradigm
It's not about the virtual dom: it's about the programming paradigm it creates.  

##### Calling a Web API
Use a WebAPIUtils module to encapsulate XHR work.  

##### More Flux Patterns
LoggingStore. It's like user analytics for free.  
Error handling with client id/dirty bit  
Error handling with actions queue  
Resolving dependencies in the Controller-view  

##### Anti-patterns
Application state/logic in React components  
Getters in render()  
Public setters in stores & the setter mindset trap  
Props in getInitialState()  
