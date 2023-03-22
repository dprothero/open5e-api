---
layout: page
title: Conditions
---

# Conditions
This is an object representation of the conditions added to the open5e-api database. You can retrieve conditions to see their description.

## Condition List
> GET /conditions

Retrieves a list of conditions objects.

### Filters
The following filtering options are available. When multiple filters are used, they are combined with AND logic.

| field | exact | iexact | in | range | icontains |
|---|---|---|---|---|---|
|  **name** | supported  | unsupported | unsupported | N/A | unsupported |
|  **document_slug** | supported  | unsupported | unsupported | N/A | unsupported |

For more information on filtering, see the [Filtering] page.

### Ordering
{% include_relative standard-ordering.md %}

## Condition Object
> GET /condition/:slug

Retrieves the condition object referenced by the slug.

## Attributes
**desc** string

A description of how a creature is impacted while the condition is imposed on them.

### Standard Attributes
{% include_relative standard-attributes.md %}