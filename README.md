# EGA KNP JSON Schema samples

This is a WIP/for review format mostly done to show what a simple JSON schema is. Before working more on the format (
defining encoding, required fields, allowed values, fields layout, etc.) we should define the meaning of each field (
usage and values) at a higher level using, for example,
a [Domain Driven Design](https://en.wikipedia.org/wiki/Domain-driven_design) approach.

## Pointers

* The [JSON Schema](https://json-schema.org/)
* A simple online [JSON Schema Validator](https://json-schema.org/)
* Language codes: [IETF BCP 47](https://en.wikipedia.org/wiki/IETF_language_tag), also specified
  in [W3 language tags](https://www.w3.org/International/articles/language-tags/) and the
  original [BCP 47 Note](https://www.rfc-editor.org/rfc/bcp/bcp47.txt).
* There is an unofficial [online BCP 47 validator](https://schneegans.de/lv/) that also provide a regular expression to
  validate code format. We may use the same approach to enforce allowed language code since JSON Schema also
  support [regular expression pattern](https://json-schema.org/understanding-json-schema/reference/regular_expressions.html)
  .
* [JSON Schema date and time](https://json-schema.org/understanding-json-schema/reference/string.html#dates-and-times)
  represented in [RFC 3339, section 5.6](https://tools.ietf.org/html/rfc3339#section-5.6). This is a subset of the date
  format also commonly known as [ISO8601 format](https://www.iso.org/iso-8601-date-and-time-format.html).
* [Netflix KNP Tool](https://partnerhelp.netflixstudios.com/hc/en-us/articles/115000676891-KNP-Tool-Overview) and
  its [Template](https://docs.google.com/spreadsheets/d/11u-tsOJq1r2HJy_ds7pD95C-Vy9jKEfT5wTYhhtNHAg/edit#gid=1062876492)

## Some thought

* Should we enforce id? For example using [UUID](https://en.wikipedia.org/wiki/Universally_unique_identifier) or even
  better [ULID](https://github.com/ulid/spec)?
* Should we try to track changes using a more elaborate revision field?
* Should we allow more fine grain locking state?
* Should we expose "humanized labels"?
* Should we allow markdown in text fields, especially for a nice render of links?
* How to ensure a safe conversion between a JSON and a spreadsheet?