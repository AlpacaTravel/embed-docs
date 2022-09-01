# Standard Embed

## Basic Usage

By using the following script tag in your HTML, the embed will automatically
place the embed on to your page.

```html
<!-- Include an itinerary at the location of the script tag -->
<script
  type="text/javascript"
  src="https://made.withalpaca.travel/v3/embed/itinerary/123"
  async
></script>
```

This script tag is placed within your HTML at the desired location to place
the embed.

## Script Behaviour

The script will automatically create a container `HTMLDivElement` on your page,
and then assign some of the basic inline styles upon it.

When loaded, the script will then use matching information it is configured
with, including the detected device type as well as the container sizing,\
in order to identify the correct embed to use.

The script also adds a `ResizeObserver` to the container element, in order to
automatically re-evaluate the container element sizing and the corresponding
iframe in the case that a resize event occurs.

If a different size embed is required, a new `HTMLIFrameElement` may be
composed in order to mount the embed within the container.

The contents of the container element are replaced with the content as
determined by the script.

### Container Element

The `HTMLDivElement` is created as the outer container element for the
embed, and is for containing the correct embed option.

By default, without any configuration the script will automatically create
the element as an immediate sibling to the script tag.

```html
<!-- Example of the container element created automatically -->
<!-- Note: You do not need to add this element yourself -->
<div id="alpaca_itinerary123" class="alpacaContainer" style="...">...</div>
```

The container element is then applied some basic style elements which are
common to try and style the element as best it can for your HTML document.

Typically, the CSS applied is `display: float; min-height: 600px`, although this
can change.

#### Custom Container

You may also wish to create your own container element in which the script
should place the embed within.

```html
<!-- My custom container -->
<div id="my_container" style="display: block; min-height: 500px"></div>

<!-- Tell the script tag to mount into my_container -->
<script
  type="text/javascript"
  src="https://made.withalpaca.travel/v3/embed/itinerary/123"
  data-container-id="my_container"
  async
></script>
```

By doing this, the script will not create a container element with any styles.
Instead you will take on control over the CSS styling of the element.

You can then use CSS within your HTML page in order to best fit the element
within your HTML.

### IFrame Element

In circumstances, an `HTMLIFrameElement` element used to draw in the embed
content.

```html
<!-- Example of HTML IFrame element created by the script -->
<!-- Note: You do not need to add this element yourself -->
<iframe
  src="https://made.withalpaca.travel/..."
  allow="geolocation"
  class="alpacaEmbed"
  style="..."
/>
```

The iframe will be added as the child of the container element, replacing
any of the existing content with this element.

Typically, the CSS applied is `flex: 1; border: 0`, although this can change.

## CDN and Caching

Alpaca serves the script tag via its' CDN service in order to make this script
available at speed to your visitors.

The CDN service will automatically serve the correct version of the script to
your audience, based on the detected device type (such as mobile or desktop).

As a result, you should not download the script or attempt to cache the script
yourself.