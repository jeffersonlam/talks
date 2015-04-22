# Design + Performance
Steve Souders (SpeedCurve)  
11:15am–11:45am Wednesday, 04/22/2015  
Interface and experience design  

## Notes
Goal: To bring developers and designers closer together  
This is what might happen: a pillow fight (minus the pillows)  
> "I used to be a reckless designer." - Yesenia Perez-Cruz (Philadelphia, PA)
Beautiful designs, awful performance
* Requests: 136
* Page weight: 5.9mb
* Load time: 2m46s
Bad performance means the web page is less enjoyable for users.  
Obama's fundraising platform: 60% performance increase => 16%+ conversion rate  

As is:
* Designers & devs often work in silos
* 
* moving fast is important

Solutions:
* Have small interdisciplinary teams.
  If you have a design/concept and then bring in devs later, they're already behind.
* Speed is more important than design embellishment.
    * Users expect sites to render in under 2 seconds
    * People are filling small gaps in their day with news. It must load fast on all touchpoints.
* Prototype early
    * Make them **real**, not just smoke and mirrors.
    * Work with real news sources.
* Measure performance from the start
    * Define performance budgets
    * In-page reminders (Etsy)
        * Show clear baseline of what's acceptable
        * Serves as a constant reminder to the team about performance
* Don't rely on window.onload() as a metric. That's being overly optimistic.
    * Amazon: 99% ATF rendered: 2.0s. Window.onload(): 9.7s

Tools for performance test
* Webpagetest
    * Look at the **Start Render** and **Speed Index** time, not page load time.
    * Speed index: the median (middle) pixel of the ATF content.
    * Show the results to your team, and the effect performance has on user experience will become apparent

Question: How do we figure out when an image gets displayed on the screen?


## Action Items
* [ ] Start utilizing Webpagetest within the design process
* [ ] Implement an in-page reminder of performance in prototypes
