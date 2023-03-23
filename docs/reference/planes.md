---
layout: page
title: Planes
---

# Planes
This is an object representation of the planes of existence added to the open5e-api database. You can retrieve planes to see their description.

## Plane List
> GET /planes

Retrieves a list of plane objects.

### Filters
The following filtering options are available. When multiple filters are used, they are combined with AND logic.

| field | exact | iexact | in | range | icontains |
|---|---|---|---|---|---|
|  **name** | supported  | unsupported | unsupported | N/A | unsupported |
|  **document_slug** | supported  | unsupported | unsupported | N/A | unsupported |

For more information on filtering, see the [Filtering] page.

### Ordering
{% include_relative standard-ordering.md %}

## Plane Object
> GET /plane/:slug

Retrieves the plane object referenced by the slug.

## Attributes
**desc** string

A description of the plane of existence.

### Standard Attributes
{% include_relative standard-attributes.md %}