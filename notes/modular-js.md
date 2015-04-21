
---

"How can we create a consistent, updateable user experience across all devices?"  
UI <-> Platform  
Kind of like UI <-> Browser  
Netflix History: They built their first UI off Webkit (browser-based).  
Then they thought: do we really need all that browser stuff?  

They built their own platform for distributing that UI.  
What they needed in that platform:
* Video Decoding & Playback
* Networking
* Logging
* Crypto & Security
* Content-Control and Caching
* Adaptive Streaming

Problem with Object-Oriented Languages: You want the banana, but you get the gorilla carrying the banana, along with the entire jungle.  
All programming languages: You should really maintain independence from all the systems in which your code lives.  
modules, commonJS Style  
  var videoMgr = require('...');  
  ES6 has this built in.  

Modular Programming is a subset of procedural programming.
