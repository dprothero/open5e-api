---
layout: page
title: Feats
---

# Feats
This is an object representation of feats added to the open5e-api database. You can retrieve feats to see their description.

## feat List
> GET /feats

Retrieves a list of feat objects.

### Filters
The following filtering options are available. When multiple filters are used, they are combined with AND logic.

| field | exact | iexact | in | range | icontains |
|---|---|---|---|---|---|
|  **name** | supported  | unsupported | unsupported | N/A | unsupported |
|  **document_slug** | supported  | unsupported | unsupported | N/A | unsupported |

For more information on filtering, see the [Filtering] page.

### Ordering
{% include_relative standard-ordering.md %}

## Feat Object
> GET /feat/:slug

Retrieves the feat object referenced by the slug.

## Attributes
**desc** string
The first line of the description of a given feat.

**prerequisite** null or string
A description of any prerequisites that need to be met for the feat to be applied.

**effects_desc** list of strings
A list of effects that would be imparted on your character upon gaining the feat.

### Standard Attributes
{% include_relative standard-attributes.md %}