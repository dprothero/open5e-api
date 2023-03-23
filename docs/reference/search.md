---
layout: page
title: Search
---

# Search
This is an endpoint that allows for searching certain fields in our database for a string. All models are available for search.

## Results List
> GET /search

Retrieves a list of all searchable objects. To search across many fields for text, use the special parameter **text**.

### Filters
All public fields are available for filter. When a filter is applied to a search, it excludes objects that do not have the field. See examples below.

For more information on filtering, see the [Filtering] page.

## Attributes

For each result, all object attributes return as part of the search results. In addition, there are a few special fields returned in search results.

**text** string

A string representation of the object. Usually a concatenation of the **name** field (or **title** in some cases) and the **desc** field.

**highlighted** string html

A preview of html text with the search term highlighted in it.

**route** string

The object route (part of the URL) for navigation. 

### Standard Attributes
{% include_relative standard-attributes.md %}

### Examples

> GET /search/?text=missile&name=magic

Returns both the spell "Magic Missile" and the magic item "Wand of Magic Missiles".

> GET /search/?text=dragon&rarity=rare

Returns 3 magic items related to dragons. This is an inefficient way to search multiple fields in a single request.
