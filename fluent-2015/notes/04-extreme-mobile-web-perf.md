# Extreme Performance for Mobile Devices
[Maximiliano Firtman (ITMaster Professional Training)](http://www.firt.mobi/)  
[Details](http://fluentconf.com/javascript-html-2015/public/schedule/detail/39394)  
[Slides](http://firtman.github.io/fluent/)  
Learn about web standards for mobile web performance, and strategies for how to achieve these standards.  

## Notes
Q: What are today's web platforms?  
A: You'd probably say "iOS and Android". But it's not so simple.
- iOS: 50%
  - Apps (Web View) 12% (it's not exactly Safari)
    - Safari 88%
      - versions: 6.x 2%, 7.x 19%, 8.x 79%
- Android
  - "Android Browser" 50%
    - Chrome 50%

#### Mobile Web Today
> "Be sure to think about the average user. All of us here are not average users."  
"As is the nature of the web, everything will change. Embrace the change."  
"You might be losing users if responsive design is your only mobile strategy."  

- Perception
  - immediate feedback <100ms
  - keeping user's flow of thoughts <1s
  - 500ms delay, +26% user's frustration

Q: Why do we need special consideration for mobile?
A: CPU, GPU, and Memory

- The average user: the difference is in 5x (cpu, gpu, memory)  
- Wifi
    - and wifi public spaces
        > "You know how wifi works in public spaces."

Cellular connections

"But that will change quickly."
    2019: 95% of the US and Europe will have 4G.
    4 years.
"Latency is always there."
    Latency is our biggest problem, and it's not going anywhere.

#### Performance & Mobile
> *insert gif here* "That's you working on a responsive web design."  
"Responsive Web Design is a tool. It's not a goal."  
"Users don't care if your site is responsive."  
"Users DO care if the site is FAST."  

- Perception: 1s threshold
- RTT latency
- Test on low hardware and 2G/3G
- RWD harms performance


#### Mobile test tools
- iOS simulator will show how iOS safari behaves in the way it displays stuff. but performance, it's not the same. it's running off your mac.
- Simulators are just that: simulators. be careful, and don't trust them too much as indicators of how your websites will perform in those situations.
- Google Mobile Performance Insights
- Mobitest
- Safari. You can plug in your iPhone and test with it!
    - Do an alert in the console, and a notification will pop up on your phone
- Chrome. You can plug in your phone and do the same thing


#### Initial Loading & Perception
- 1 second threshold
- classic checklist
- rwd

5 coins:
> "We have only 1 coin for the rendering."  
"We just need the PERCEPTION that the page is there."  
"We need to avoid stop signs and please-slow-down signs."  

- JS: Blocks parsing
- CSS: Blocks rendering
- Redirects will take from 150 to 1000ms per redirect
- URL shorteners: t.co, g.co, bit.ly
- DON'T REDIRECT!

- Stop signs
  - Don't stop your user and tell them to download the app, or something.
  - "How many of you have downloaded the app from that link?"
    tweet

- Page contents in 14kb compressed
- Uncompressed: ~70kb
- Above the Fold (ATF): in less than 1 second
- ATF: 50% more than the first view there, to account for larger devices.
- Try to deliver everything in 14kb.

#### Performance for Above the Fold
- Avoid JS frameworks
    - If you add jquery, we're out!
    - embrace vanilla js
    - If you really need them, load them after TF
    think of alternatives or partial frameworks
- Careful with Data URI in CSS
    - Images are non-blocking by default
    - Using Data URI in CSS creates blocking images
    - Use them only on non-ATF external CSS
- Client side rendering
    - Careful with client-side frameworks
    - Try to render the initial view server-side
    - Render at least a basic view
- RWD
    - Media queries block rendering (all of them)
    - ATF content on mobile is unique
- Defer non-ATF resources
    - No defer or async attributes (yet)
    - Inject link after rendering

- Speed up future visits
    - be cache friendly
    - use application cache for ATF content
    - create a custom cache

#### responsiveness and experience
- Experience
- Consistent frame rate
- Immediate feedback
- Scrolling
- Your new enemy
    - YOUR DESIGNER. or yourself.

> "Sorry, I need to remove that feature, because it's taking up our money."  

- don't do CPU repaints
- embrace GPU smartly

## Action Items

- [ ] Have a "budget" for performance
- [ ] Test on real devices, not simulators
- [ ] Render ATF content first
