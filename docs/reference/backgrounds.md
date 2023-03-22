---
layout: page
title: Backgrounds
---

# Backgrounds
This is an object representation of the backgrounds added to the open5e-api database. You can retrieve backgrounds to see skill proficiencies, features, and other data points.

## Background List
> GET /backgrounds

Retrieves a list of background objects.

### Filters
The following filtering options are available. When multiple filters are used, they are combined with AND logic.

| field | exact | iexact | in | range | icontains |
|---|---|---|---|---|---|
|  **name** | supported  | unsupported | unsupported | N/A | unsupported |
|  **document_slug** | supported  | unsupported | unsupported | N/A | unsupported |
|  **skill_proficiencies** | supported  | unsupported | unsupported | N/A | unsupported |
|  **languages** | supported  | unsupported | unsupported | N/A | unsupported |

For more information on filtering, see the [Filtering] page.

### Ordering
{% include_relative standard-ordering.md %}

## Background Object
> GET /background/:slug

Retrieves the background object referenced by the slug.

## Attributes
**skill_proficiencies** string

Skills that the background provides proficiency in.

**tool_proficiencies** null or string 

Tools that the background provides proficiency in.

**languages** string

Description of languages that the background provides an understanding of.

**equipment** string

Description of equipment provided by the background.

**feature** string

Name of the feature provided by the background.

**feature_desc** string

Description of the feature provided by the background.

**suggested_characteristics** string

Description of the qualities that a character with this background may have.

### Standard Attributes
{% include_relative standard-attributes.md %}