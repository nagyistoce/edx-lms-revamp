# NOTES: Standards #

* [strat] Theming doc - https://docs.google.com/a/edx.org/spreadsheet/ccc?key=0ArjcFrBngjmkdHh1X1hhbWJIbUFMbThDd2NMbGt6SlE&usp=sharing
* [accessibility] TPG Accessibility Audit - http://cl.ly/450e3E032d3V
* [accessibility] WebAIM Color Contrast Checker - http://webaim.org/resources/contrastchecker/
* Bourbon documentation - http://bourbon.io/docs/
* Neat documentation - http://neat.bourbon.io/docs/

***

## File Structure and Page Organization ##

* place vendor assets within specific vendor directories inside of each static subdirectory (and correct any file/resource references)
* always load vendor CSS separately from app/other Sass-centric css files

***

## HTML Element Syntax and Class Names ##

* Use BEM for layout/module-level elements - http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/
* Use nested common, content/purpose-driven class names for elements inside of modules (.title, .copy, .actions)
* stateful names (is-hidden, is-shown, is-dragging, is-dropping, has-actions, is-not-loggedin, is-loggedin)
* Adhere to nesting/philosophy of http://smacss.com/

Use BEM syntax/naming conventions for page-level structural elements and for modular structure (page elements), but do not conflate modular class names with page-level structure if possible.

Use BEM syntax/naming conventions for modifiers of common class archetypes (e.g. <h2 class="title title--section"> or <nav class="nav nav--course">)

 Use BEM syntax/naming conventions for modifiers of list items to indicate specific items in a list (e.g. <li class="nav__item nav__item--progress"> vs. <li class="nav__item nav__item--wiki">)

When needing to put in additional context/indication for screen readers, assistive tech, viewports use one of the following wrapper-element classes:

1. <span class="indicator--context"> = for contextual hints
2. <span class="indicator--current"> = for noting when the current nav/content item relates to a user's current state/view

For copy that is announcement in nature, use the "statement" (e.g. statement-copyright).

Try not to use .sr utility classes to hide elements, but rather plan for them and extend the %ui-text-sr placeholder on specific elements.

For content-heavy items (messages, updates, descriptions), plan for common semantic elements (.title, .nav, .copy. .metadata, .actions). Its best to have a containing element for portions that may contain multiple items themselves (.copy p, .nav li/a, .actions li/a)

For each view, add a view--viewname class to the <body> element (e.g. view--courseupdates)
For each view, add any view, global, or historical/account-based state classes to the <body> element (e.g. is-logged-in, is-archived, is-not-loggedin)

***

## HTML Element Use ##

Use <article> elements as a component of a page that consists of a self-contained composition in a document, page, application, or site and that is intended to be independently distributable or reusable, e.g. in syndication.

Use <nav> elements only to contain lists/collections of links/pointers that would be used to navigate away/around the current view

***

## Sass Syntaxt ##
* do not nest more than three layers
* if it doesn't render directly or is shared, make it an @extend with %placeholer syntax

