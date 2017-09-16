
<!---

This README is automatically generated from the comments in these files:
iron-ajax.html  iron-request.html

Edit those files, and our readme bot will duplicate them over here!
Edit this file, and the bot will squash your changes :)

The bot does some handling of markdown. Please file a bug if it does the wrong
thing! https://github.com/PolymerLabs/tedium/issues

-->

[![Build status](https://travis-ci.org/rocketsciencesolutions/wordpress-collect.svg?branch=master)](https://travis-ci.org/rocketsciencesolutions/wordpress-collect)

## &lt;wordpress-collect&gt;

The `wordpress-collect` element makes it possible to interact with the native [WP REST API](https://developer.wordpress.org/rest-api/reference/).

```html
<wordpress-collect
      base-url="https://cms.rocketscience.io"
      wp-api-url="wp-json/wp/v2"
      resource="pages"
      id="1"
      response="{{wpPages}}"></wordpress-collect>
```

The `base-url` attribute is the Wordpress url you want to retrieve the data from.
`wp-api-url` attribute is optional, this attribute will be placed after the `base-url`.
When the `wp-api-url` attribute is not defined it will always default to `wp-json/wp/v2`,
which is the default WP REST API segment. The `resource` attribute indicates the kind of resource to retrieve. This can be pages | posts or other resources defined in the [WP REST API reference](https://developer.wordpress.org/rest-api/reference/). When data is received the binding in the `response` attribute is updated with the retrieved data and available for use in the component which `wordpress-collect` is situated. In this case it can contain an Array or an Object depending on the request made.

