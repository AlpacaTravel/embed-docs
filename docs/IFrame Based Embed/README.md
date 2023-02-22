# IFrame Based Embed

## Using iframes to embed Alpaca Travel itineraries

Alpaca Travel also allows you to embed its itineraries using an iframe HTML
element. This can be a useful alternative for users who are unable to use
script-based embeds due to limitations in their CMS or platform.

In addition to providing an oEmbed API endpoint, Alpaca Travel also allows you
to embed its itineraries using an iframe HTML element. This can be a useful
alternative for users who are unable to use script-based embeds due to
limitations in their CMS or platform.

To use the iframe-based embed option, you can simply construct an `<iframe>` tag
with the appropriate src attribute. For example, to embed the itinerary with ID
`itnerary/12345`, you can use the following URL as the src attribute:

```
https://made.withalpaca.travel/embed/itinerary/12345
```

This will load the itinerary as an iframe within your website. However, it's
important to note that using iframes has some trade-offs. You will have limited
control over the responsive behavior of the embed, and will need to style and
size the iframe element yourself to fit your website. This can be more
challenging for non-technical users.

If you're having trouble with the script-based embed option, it may be worth
speaking to your web development team about extending your CMS to allow you to
paste in HTML, or adding oEmbed protocol support. This can provide a more
flexible and user-friendly way to embed Alpaca Travel itineraries into your
website.

## Example HTML for iFrame

The below example uses HTML elements of an `<iframe>` and a surrounding `<div>`
tag to size and position the content.

```html
<div
  style="
    min-height: 600px;
    max-height: 800px;
    width: 100%;
    aspect-ratio: 4/3;
    position: relative;
  "
  class="alpacaContainer"
>
  <iframe
    allow="geolocation"
    width="1280"
    height="720"
    src="https://made.withalpaca.travel/embed/itinerary/458UEs3vKr8asSekgzPcKg"
    style="width: 100%; height: 100%; position: absolute;"
    frameborder="0"
  ></iframe>
</div>
```
