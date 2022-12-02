# Google Analytics

Using the Google Analytics integration option of the Alpaca Platform provides
a mechanism to report on visitor interaction with content through the Embeds.

The following guide is provided for reference around the behaviour of the
Google Analytics integration.

Some notable details:

- Alpaca can push events to Google Analytics to GA4 Properties
- Alpaca uses integration via `gtag.js` which will push to `Data Stream` using
  supplied `Measurement ID`
- Alpaca, in a typical Single Page Application (SPA), will disable
  automatic `page_view` events. Events are then created each page change with
  the additional event parameters to enhance the associated context of events.

Google Analytics properties may need additional configuration, such as setting
up Event Mapping or the use of Custom Definitions to access all data sent to the
Data Stream within Google Analytics.

Note: Please be aware that this reference and implementation is subject to
change.

## Page View

Alpaca will attempt to propagate a `page_view` event with the following
core parameters:

| Parameter name   | Note                                                    |
| ---------------- | ------------------------------------------------------- |
| `page_location`  | The page location                                       |
| `page_title`     | the page title                                          |
| `content_group`  | The Itinerary title                                     |
| `content_group2` | The Profile Name of the author of the content           |
| `content_group3` | The type of itinerary (e.g. `list`, `trail` and `trip`) |

Note: The core parameters are intended to be uniform in the way that they are
propagated to GA4 and may not match the exact SPA title or page URL.

## View item

Alpaca will attempt to propagate a `view_item` event with a `items` parameter
that contains information about the viewed item assigned to Google Analytics
parameters.

| Item parameter   | Note                                                                |
| ---------------- | ------------------------------------------------------------------- |
| `item_name`      | Content title                                                       |
| `item_id`        | The unique ID associated with the content (e.g. `itinerary/abc123`) |
| `item_brand`     | The name of the profile                                             |
| `item_category`  | The profile name associated with the itinerary                      |
| `item_category2` | The type of itinerary, such as `list`, `trail` and `trip`)          |
| `item_category3` | The itinerary name, when viewing a location                         |

## Alpaca Custom Events

Alpaca will send events through a custom event, named `alpaca`. Along with the
event, Alpaca includes the following parameters:

| Parameter name            | Note                                       |
| ------------------------- | ------------------------------------------ |
| `alpaca_method`           | The event name                             |
| `alpaca_method_namespace` | The event name, with a prefix of `alpaca_` |

Alpaca recommends that users set up Event Mapping that will remap the
`alpaca_method` or `alpaca_method_namespace` to the Event name.

Events include:

- `impression`: Occuring along with `page_view` events
- `indicated`: Occuring when users interact with content (such as resulting
  from `hover` events)
- `map_interaction`: Occuring when users interact with the map (such as
  resulting from `dragend`, `boxzoomend`, `mouseup`, `touchend`)

## Contextual Parameters

Along with core events, Alpaca will attempt to provide additional content to
events:

| Parameter name                            | Note                                                       |
| ----------------------------------------- | ---------------------------------------------------------- |
| `alpaca_profile_id`                       | The Profile ID of the author of the content                |
| `alpaca_source_id`                        | The Itinerary ID for the content                           |
| `alpaca_source_type`                      | The type of content (`itinerary`)                          |
| `alpaca_source_title`                     | The Itinerary title                                        |
| `alpaca_view`                             | The layout used to present the content                     |
| `alpaca_source_attribute_external_ref`    | The supplied external ref associated with the itinerary    |
| `alpaca_source_attribute_external_source` | The supplied external source associated with the itinerary |
