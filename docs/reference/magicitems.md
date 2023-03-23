---
layout: page
title: Magic Items
---

# Magic Items
This is an object representation of the magic items added to the open5e-api database. You can retrieve magic items to see rarity, description, and other data points.

## Magic Items List
> GET /magicitems

Retrieves a list of magicitem objects.

### Filters
The following filtering options are available. When multiple filters are used, they are combined with AND logic.

| field | exact | iexact | in | range | icontains |
|---|---|---|---|---|---|
|  **name** | supported  | unsupported | unsupported | N/A | unsupported |
|  **document_slug** | supported  | unsupported | unsupported | N/A | unsupported |

For more information on filtering, see the [Filtering] page.

### Ordering
{% include_relative standard-ordering.md %}

## Magic Item Object
> GET /magicitems/:slug

Retrieves the magic item instance referenced by the slug.

## Attributes
**type** string

One of "Wondrous item" or a basic description of the item type, such as "Weapon (any sword)".

**desc** string 

A description of the item.

**rarity** null or int

One of "common", "uncommon" or "rare", "very rare" or "legendary".

**requires_attunement** string

Empty string or "requires attunement".


### Standard Attributes
{% include_relative standard-attributes.md %}