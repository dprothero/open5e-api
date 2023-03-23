---
layout: page
title: Sections
---

# Sections
This is an object representation of the text sections items added to the open5e-api database. These sections are multi-line descriptions of game concepts.

## Section List
> GET /sections

Retrieves a list of section objects.

### Filters
The following filtering options are available. When multiple filters are used, they are combined with AND logic.

| field | exact | iexact | in | range | icontains |
|---|---|---|---|---|---|
|  **name** | supported  | unsupported | unsupported | N/A | unsupported |
|  **document_slug** | supported  | unsupported | unsupported | N/A | unsupported |

For more information on filtering, see the [Filtering] page.

### Ordering
{% include_relative standard-ordering.md %}

## Section Object
> GET /sections/:slug

## Attributes

**desc** string markdown

A long-form description of a game concept. As an example, the mechanics of diseases are explained in detail in a section.

**parent** string

Describes the category of the section. Current categories are:
* Equipment
* Characters
* Rules
* Character Advancement
* Appendix
* Spellcasting


### Standard Attributes
{% include_relative standard-attributes.md %}