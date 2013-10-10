# NOTES: Standards #

* [strat] Theming doc - https://docs.google.com/a/edx.org/spreadsheet/ccc?key=0ArjcFrBngjmkdHh1X1hhbWJIbUFMbThDd2NMbGt6SlE&usp=sharing
* [accessibility] TPG Accessibility Audit - http://cl.ly/450e3E032d3V
* [accessibility] WebAIM Color Contrast Checker - http://webaim.org/resources/contrastchecker/
* Bourbon documentation - http://bourbon.io/docs/
* Neat documentation - http://neat.bourbon.io/docs/

***

## HTML Class Names ##

* Use BEM for layout/module-level elements - http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/
* Use nested common, content/purpose-driven class names for elements inside of modules (.title, .copy, .actions)
* stateful names (is-hidden, is-shown, is-dragging, is-dropping, has-actions, is-not-loggedin, is-loggedin)
* Adhere to nesting/philosophy of http://smacss.com/

***

## Sass Syntaxt ##
* do not nest more than three layers
* if it doesn't render directly or is shared, make it an @extend with %placeholer syntax

