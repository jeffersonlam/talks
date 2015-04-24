# Responsive Typography: The Foundation of Great Performance and Design
Jason Pamental (Fresh Tilled Soil)
[Github](https://github.com/jeffersonlam/rwt-fluent)


#### life of <p>
-You can pull text snippets and retain their formatting by using paragraph tags as visual indicators.
-text indent: 1em
-last line without any orphans.
  -use widotamer
    wt.fix({
        elements: 'p',
        chars: 10,
        method: 'nbsp',
        event: 'resize'
    });

#### a dash of dashes
-justification with hyphenation
-hyphenation without justification
-in a smaller screen, with or without justification is awful. but hyphenation looks good.
.hyphens{
    word-wrap: break-word;
    -webkit-hyphens: auto;
    -moz-hyphens: auto;
    -ms-hyphens: auto;
    -o-hyphens: auto;
    hyphens: auto;
    text-align: justify;
}

#### i can read for miles and miles and...
    -it's difficult to read really long lines. better to set a max width
    p{
        max-width: 38em;
    }

#### drop it like a cap
    -you can stylize the first letter of a passage with something like this
        p:first-of-type:first-letter, .lt-ie9 p:first-letter{
            font-size: 5em;
            font-family: ;
            color: 5em;
            line-height: 0.9em;
            float: left;
            padding-right: 0.05em;
            margin-top: -0.125em;
        }

#### first line of defense
    -bold the first line in a passage
        p:first-line{
            font-size: 1.1em;
            font-weight: bold;
        }

#### link it, link it good
    -"This is a screenshot from chrome, and that's a really ugly link."
    -we can do border bottom... we can do a dotted line... but that's all we can do. until recently.
    -Medium made a beautiful solution
    .nicelink{
        font-size: 5em;
        tex-tshadow: ...
        background-image: ...
        background-repeat: ...
        background-size: ...
        background-position: ...
        display: inline;
        word-break: break-word;
    }

"We're trying to add some grace to the reading experience without sacrificing clarity or readability."

-a flair for the dramatic
-every once in a while, it's ok for that answer to be more beauty and grace.
-we wanna make sure that final layer between you and the user as polished and seamless as possible.
    .otf{
        ...
        font-feature-settings: "dlig" 1, "liga" 1;
    }

performance!
-much ado & giving us nothing
-the web: delivering content to people in the fastest and most universal way possible.
("Nothing about me is original.")
much ado & on our merry way
p{
    font-family: "playfair display", serif;
    font-size: 1.5em;
}
.wf-inactive p{
    font-family: "Times New Roman", serif;
    font-size: 1.575em;
    letter-spacing: 0.1px;
}

question: "what is the perfect <p>?"
answer: "the right one for your project"

-Seattle Times
    it works for them
-Buzzfeed
    it works for them
-The Shape of Design
    -streamlined reading experience without any interruptions, and just gentle nudges for each paragraph."
