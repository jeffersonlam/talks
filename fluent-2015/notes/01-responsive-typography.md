# Responsive Typography: The Foundation of Great Performance and Design
[Jason Pamental (Fresh Tilled Soil)](http://www.freshtilledsoil.com/)  
[Details](http://fluentconf.com/javascript-html-2015/public/schedule/detail/39224)  
[Slides](http://www.slideshare.net/jpamental)  
[Github](https://github.com/jeffersonlam/rwt-fluent)  

A crash course on thinking about, and implementing, the reading experience of your design.  

## Notes
#### life of `<p>`
* You can pull text snippets and retain their formatting by using paragraph tags as visual indicators.
* text indent: 1em
* last line without any orphans.
  * use widotamer

#### a dash of dashes
* justification with hyphenation
* hyphenation without justification
* in a smaller screen, with or without justification is awful. but hyphenation looks good.
```
.hyphens {
    word-wrap: break-word;
    -webkit-hyphens: auto;
    -moz-hyphens: auto;
    -ms-hyphens: auto;
    -o-hyphens: auto;
    hyphens: auto;
    text-align: justify;
}
```

#### i can read for miles and miles and...
* it's difficult to read really long lines. better to set a max width
```
p {
    max-width: 38em;
}
```

#### drop it like a cap
* you can stylize the first letter of a passage with something like this
```
p:first-of-type:first-letter, .lt-ie9 p:first-letter{
    font-size: 5em;
    font-family: ;
    color: 5em;
    line-height: 0.9em;
    float: left;
    padding-right: 0.05em;
    margin-top: -0.125em;
}
```

#### first line of defense
* you can bold the first line in a passage
```
p:first-line{
    font-size: 1.1em;
    font-weight: bold;
}
```

#### link it, link it good
* "This is a screenshot from chrome, and that's a really ugly link."
* We can do border bottom, we can do a dotted line, but that's all we can do. Until recently.
* Medium made a beautiful solution
```
.nicelink {
    font-size: 5em;
    tex-tshadow: ...
    background-image: ...
    background-repeat: ...
    background-size: ...
    background-position: ...
    display: inline;
    word-break: break-word;
}
```

#### ligatures
```
.otf {
    ...
    font-feature-settings: "dlig" 1, "liga" 1;
}
```

> "We're trying to add some grace to the reading experience without sacrificing clarity or readability."

> "When we're asked why something is part of a deisgn, every once in a while, it's ok for that answer to be for more beauty and grace."

> "We wanna make sure that final layer between you and the user as polished and seamless as possible."


Question: "what is the perfect `<p>`?"  
Answer: "the right one for your project"  

Examples: 
- Seattle Times
    - it works for them
- Buzzfeed
    - it works for them
- The Shape of Design
    - "...streamlined reading experience without any interruptions, and just gentle nudges for each paragraph."

## Action Items
- [ ] Think about the reading experience when designing websites. What's the right reading experience for your user? How does it compare to reading a book?  
- [ ] Utilize special CSS properties and selectors, like `first-line`, `first-letter`, `text-indent`
