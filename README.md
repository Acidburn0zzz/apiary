
# Apiary

*Nice little JS libraries sprout here.*

This is a collection of small JavaScript libraries or utilities leveraging the W3C API.
These JS modules are intended to be used from W3C pages: domain pages, group pages, personal pages, etc.
Examples of use are also included.

Refer to [the W3C API](https://github.com/w3c/w3c-api) and [its documentation](https://api-test.w3.org/doc) for details.

## Getting started (quickly)

1. Include this in your page:  
  ```html
  <script src="//www.w3.org/scripts/jquery/2.1.4/jquery.min"></script>
  <script src="scripts/domain-or-group-info.js"></script>
  ```
2. Specify the ID of the *entity* you want, adding a *data-\** attribute to the `html` element, eg:  
    ```html
    <html data-domain-id="41381">
    ```
3. Write *placeholders* wherever you'll need real data about that *entity*, eg:  
    The lead of this domain is: <span class="w3capi w3capi-lead"></span>.

## Reference

The `html` element should have one of these two *data-\** attributes: `data-domain-id`, `data-group-id`.

A placeholder is any element with a class beginning with `w3capi-`.
Bear in mind that a new chunk of DOM will be inserted there; whatever that placeholder contains will be lost.
We recommend that you have something in there giving users a hint that data is being loaded dynamically.
For example:

```html
<div class="w3capi w3capi-chairs">[Loading…]</div>`.
```

These are the supported placeholders, the types of entities they apply to, and the kind of content they generate:
* `w3capi-name` (*domain*, *group*): text
* `w3capi-lead` (*domain*): text
* `w3capi-activities` (*domain*): unordered list
* `w3capi-type` (*group*): text
* `w3capi-description` (*group*): text
* `w3capi-chairs` (*group*): unordered list

The class `w3capi` isn't used by the JS libraries themselves, but we recommended you add anyway it to all placeholders for easier CSS styling.

## Credits

Copyright © 2015 [World Wide Web Consortium](http://www.w3.org/)

This project is licensed [under the terms of the MIT license](LICENSE.md).

