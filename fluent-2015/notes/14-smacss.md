# SMACSS Your Sass Up
Mina Markham (IBM Design)  
2:15pm–2:45pm Tuesday, 04/21/2015  

## Notes

"CSS is ~~easy~~ hard"  
"CSS is bullshit."  
We can make it easier to write CSS by thinking of it as modular components.  
"This is not a homepage. This is a collection of modules that make up the homepage."  

##### SMACSS (Scalable & Modular Architecture for CSS)

categorize css rules  
meaningful names  
shallow selectors  
smacss.com  

##### Add some Sass
Namespacing
* &
* &_ or &-
Inception rule: Stay less than 3 levels deep  
Extends  
* @extend (class)  
* %(class)
  Placeholder element. Makes an element available to be extended, but not be usable by itself
  * Don't @extend between modules

Partials
  * @import
* Utilities
* Libraries
* Base
* (4)
* (5)
* States
* @font-face
* Print

shame.css  
_shame.scss
  because hacks happen

[Mina's Sassy Starter Repo](https://github.com/minamarkham/sassy-starter)

http://minamarkham.github.io/sassy-starter/
```
+ scss/
  |
  | + base/                 # reset, typography, site-wide
  |   |-- _index.scss       # imports for all base styles
  |   |-- _base.scss        # base styles
  |   |-- _normalize.scss   # normalize v3.0.1
  |
  | + layout/               # major components, e.g., header, footer etc.
  |   |-- _index.scss       # imports for all layout styles
  |
  | + modules/              # minor components, e.g., buttons, widgets etc.
  |   |-- _index.scss       # imports for all modules
  |
  | + states/               # js-based classes, alternative states e.g., success or error state
  |   |-- _index.scss       # imports for all state styles
  |   |-- _states.scss      # state rules
  |   |-- _print.scss       # print styles
  |   |-- _touch.scss       # touch styles
  |
  | + themes/               # (optional) separate theme files
  |   |-- beccapurple.scss  # rename to appropriate theme name
  |
  | + utilities/            # non-CSS outputs (i.e. mixins, variables) & non-modules
  |   |-- _index.scss       # imports for all mixins + global project variables
  |   |-- _fonts.scss       # @font-face mixins
  |   |-- _functions.scss   # ems to rems conversion, etc.
  |   |-- _global.scss      # global variables
  |   |-- _helpers.scss     # placeholder helper classes
  |   |-- _mixins.scss      # media queries, CSS3, etc.
  |   |-- _lib.scss         # imports for third party styles
  |   |-- + lib/            # third party styles
  |       | _pesticide.scss # CSS pesticide
  |       | ...
  |
  |   + ie.scss             # IE specific Sass file
  |   + styles.scss         # primary Sass file
  |   + _shame.scss         # because hacks happen
  |
  + .htaccess               # Apache server configs
  + config.rb               # Compass configuration file
  + crossdomain.xml         # cross-domain requests
  + docs/                   # SassDoc generated documentation
  + deploy.rb               # Capistrano configuration file
  + Gruntfile.js            # Grunt configuration & tasks
  + package.json            # Grunt metadata & dependencies
```

## Action Items
* [ ] Utilize the SMACSS architecture for cleaner, more modular CSS
