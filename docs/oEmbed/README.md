[//]: # "Title: oEmbed"
[//]: # "Weight: 5"
[//]: # "Layout: 1-col"
[//]: # "TOC: false"

# OEmbed

## What is oEmbed?

oEmbed is a protocol that allows websites to display embedded content, such as
videos or images, from another website without requiring the website owner to
host the content themselves. Instead, the website can request the embedded
content from the other website's oEmbed API endpoint.

## How to use Alpaca Travel's oEmbed API

### oEmbed Discovery

Alpaca Travel also follows the oEmbed Discovery specification by including
`<link rel="alternative" ... />` tags in the HTML of its itinerary pages. This
can make it even easier for CMS's and plugins to discover and use the oEmbed
information for Alpaca Travel itineraries.

With this tag in place, a CMS or plugin can simply provide the URL of the Alpaca
Travel itinerary page, and the oEmbed information will be discovered
automatically. This can greatly simplify the integration of Alpaca Travel
itineraries into a website, making it easier for developers to add dynamic,
engaging content to their site.

### Manually Calling oEmbed service

Alpaca Travel's oEmbed API endpoint is
`https://www.alpaca.travel/api/v3/oembed`. You can provide any URL scheme
matching `https://made.withalpaca.travel/view/itinerary/*` to retrieve an oEmbed
response. Here's an example of how to use the API endpoint in JavaScript:

```javascript
const url = "https://made.withalpaca.travel/view/itinerary/12345";
const endpoint = `https://www.alpaca.travel/api/v3/oembed?url=${url}`;

fetch(endpoint)
  .then((response) => response.json())
  .then((data) => {
    // Do something with the oEmbed response
  });
```

This example fetches the oEmbed response for an Alpaca Travel itinerary with ID
"itinerary/12345". You can replace the ID with any valid itinerary ID.

## Learn more about oEmbed

To learn more about the oEmbed protocol, you can visit the official oEmbed
website at [oembed.com](https://oembed.com). There, you can find more
information on how to implement oEmbed on your website.

## Using oEmbed with your CMS

oEmbed is a powerful tool that can help make your website more dynamic and
engaging. It's worth having the capability added to your custom or open-source
CMS, and it's supported by most major platforms either natively or through a
plugin. Check your CMS's documentation to see if it supports oEmbed, and if it
does, consider enabling it to allow for easy embedding of content from other
websites.
