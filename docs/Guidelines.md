[//]: # "Title: Integration Guidelines"
[//]: # "Weight: 1"
[//]: # "Layout: 1-col"
[//]: # "TOC: false"

# Guidelines for Embedding Interactive Maps

> To ensure optimal user engagement and seamless experience, designers and
> developers need to understand how to effectively structure their templates
> when embedding interactive maps on their webpages.

## Enhancing User Engagement with Interactive Maps

Interactive maps are a powerful tool that enhances user engagement and increases
the time spent on your site. They serve as actionable content elements, offering
users valuable context that can be incorporated into their planning. This makes
your content more interactive and compelling.

- Use maps for improved engagement over plain text and images.

- Position the map "above the fold," ensuring it's one of the first elements the
  user sees.

## Essential Template Customizations and Best Practices

<aside class="info">
  Customizing your template is not just an aesthetic choice, it is an integral part of best practices. This not only enhances content presentation but also boosts engagement and optimizes content outcomes.
</aside>

Embeds and scripts are common on blog posts and standard content pages. Here are
some best practices to follow:

- **DO: Allocate a dedicated space for the embed within a page.** The embed and
  its presentation should be an integral part of your template, not just pasted
  into a text block.

- **DO: Position the embed towards the top of the page.** Data shows that
  content performs better when the embed is placed higher up. Avoid making users
  scroll to the bottom to locate the embed.

- **DO: Provide ample space for the map.** Avoid constraining the map within a
  narrow text column. Providing a larger display area allows for better
  interactivity and enhances the visual appeal of your content.

- **DO: Create Space and Separation Around the Map.** To ensure that the
  interactive map stands out and doesn't blend in with the surrounding text,
  it's important to create clear delineation between the text content and the
  map embed. Utilize white space effectively, particularly in mobile displays
  where the map might be adjacent to lists or other elements. Consider the
  embed's placement relative to other text content and introduce a break or
  other distinct separator if needed to maintain clear visual separation.

- **DO: Enable Full-Screen Display with an Expand Button.** Enhance the user's
  interactive experience by allowing the map to be displayed in full screen.
  This can be achieved by placing an 'expand' button next to the map. When
  clicked, the button should stretch the map to cover the entire screen,
  overlaying all other content. Ensure there's a 'close' button within this
  full-screen mode that allows users to exit and return to their original spot
  on the page. This full-screen feature not only enhances the interactivity of
  the map but also gives users a more immersive experience.

- **DO: Provide a fullscreen template.** Create a site template that allows the
  map to display at full width and height (under your navigation). This can
  enable users to view the map in full-screen mode.

- **DO: Facilitate easy addition of embeds to a page.** Adhere to content
  management best practices and separate the content from its presentation.
  Request only the itinerary ID from your CMS user and integrate the tested and
  appropriately styled code.

## Content Management Recommendations

Incorporate support for embeds at the content management system (CMS) level to
aid users in adding content.

- We suggest avoiding reliance on `code blocks` or `iframe` for integration.
  While these can be useful, they often restrict the embed to a smaller template
  region and can manipulate the code, such as removing script tags.

- Users should be able to add content via the CMS using a custom content field
  or content element.

- Content creators using the Itinerary Editor receive an itinerary ID in the
  format `itinerary/XXX`. The CMS should permit users to paste in this detail.
  It's recommended to encourage users to provide only this ID.
