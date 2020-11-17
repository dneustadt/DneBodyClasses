Additional Body Classes for Shopware 6
=====

This plugin for [Shopware 6](https://www.shopware.de) adds specific classes for the current theme and sales channel
to the body tag.

It's meant to compliment the [DneCustomCssJs](https://github.com/dneustadt/DneCustomCssJs) and to allow restrictions in
CSS attributes and JS towards sales channels and/or themes.

Requirements
-----

* Shopware >= 6.3

Installation
====

* Download the `DneBodyClasses.zip` of the latest release from the [releases page](https://github.com/dneustadt/DneBodyClasses/releases).
* Upload the Zip File through Settings/System/Plugins
* Install and active the plugin

Usage
=====

After installation you can inspect the storefront and will find that body has two additional classes.

* `sc` prefixes the current ID of the Sales Channel
* `theme` prefixes the current ID of the Theme

```html
<body class="sc-375c7ac0c2654900b2503fe0ea856932 theme-416bb0456b8440368addfc1c089191ae is-ctl-navigation is-act-home">
    ...
</body>
```

You can then specifiy CSS for a specific theme or sales channel:

```scss
.sc-375c7ac0c2654900b2503fe0ea856932 {
  .example {
    color: $primary;
  }
}
```

or for restricting the execution of JS

```js
if (document.body.classList.contains('sc-375c7ac0c2654900b2503fe0ea856932')) {
  console.log('hello world');
}
```
