# Wix Editor: Adding Alpaca Travel Embeds

Wix is a popular online website editing platform, and provides various
mechanisms that can be used to embed Alpaca Travel embeds onto your website.

See Wix Support Documentation:

- [Wix Editor: Embedding a Site or a Widget](https://support.wix.com/en/article/wix-editor-embedding-a-site-or-a-widget)

## Overview

Wix refers to _Add Elements_ in which you can select to _Embed Code_. You then
select the _Popular Embeds_ and can select _Embed HTML_.

### Embed HTML: Providing the HTML/Script Tag

If you wish to use the script tag method of embedding Alpaca into the site, you
will need to use the script tag you've obtained from the Alpaca embed screen,
which should be similar to the following:

```html
<script
  type="text/javascript"
  src="https://made.withalpaca.travel/api/v3/embed/itinerary/123"
  async
></script>
```

The exact script tag may change, based on your configuration of the view options
and any sizing controls you have configured.

You can also refer to the standard embed guide in order to determine the correct
embed that you want to display.

### Embedding a Site: Using the iFrame src value

You can also attempt to use the embedding a site, and pasting the iFrame src.
