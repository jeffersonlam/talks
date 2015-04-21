# Eliminate JavaScript Code Smells
Elijah Manor (Ramsey Solutions)
4:30pm–5:00pm Tuesday, 04/21/2015
@elijahmanor
Slides: bit.ly/js-smells
---

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
