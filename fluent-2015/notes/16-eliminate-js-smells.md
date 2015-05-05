# Eliminate JavaScript Code Smells
[Elijah Manor (Ramsey Solutions)](http://elijahmanor.com/)  
[Details](http://fluentconf.com/javascript-html-2015/public/schedule/detail/39473)  
[Slides](http://elijahmanor.github.io/talks/js-smells/#/)  

Learn about web standards for developing JS, and how to avoid writing code that smells.  

## Notes
Agenda
* Easy to lint, common rules
* Easy to lint, fresh rules
* Easy to lint, no rules
* Hard to lint, subjective rules

Cyclomatic complexity

Linter rules:
* max-statements:[2, 16]
* max-depth: [2, 5]
* complexity: [2, 7]
* max-len: [2, 65]
* max-params: [2, 80]
* max-nested-callbacks: []

Resources
* jshint
* eslint
* jasmine

##### Copy and pasted code
* jsinspect
  Detect copy-pasted and structurally similar code

##### Switch statement smell
Violates the open/closed principle.  
**Uncle Bob's SOLID principles**  
Strategy design pattern  
Const & Symbols  

Linter Rules
  [Repo](bit.ly/eslint-plugin-smells)
  no-switch

* [ ] Lookup Addy Osmani JS Design Patterns
* [ ] Look up Lowdash and Underscore
* [ ] 

##### The "This" smell

##### Crisp contatentation smell
String contatentation with all the pluses and quotes. Ugly!  
Alternative: Tweet-sized contatentation

##### Inappropriate intimacy

##### More ESLint Rules
* eslint-plugin-react
* eslint-plugin-angular
* eslint-plugin-ember
* eslint-plugin-backbone
There are certain ways to write code in all these frameworks!

## Action Items
* [ ] Utilize a linter (preferably ESLint)
