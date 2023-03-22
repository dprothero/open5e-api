---
layout: page
title: Armor
---

# Armor
This is an object representation of the armor items added to the open5e-api database. You can retrieve armor to see cost, weight, and other data points.

## Armor List
> GET /armor

Retrieves a list of armor objects.

### Filters
The following filtering options are available. When multiple filters are used, they are combined with AND logic.

| field | exact | iexact | in | range | icontains |
|---|---|---|---|---|---|
|  **name** | supported  | unsupported | unsupported | N/A | unsupported |
|  **document_slug** | supported  | unsupported | unsupported | N/A | unsupported |

For more information on filtering, see the [Filtering] page.

### Ordering
{% include_relative standard-ordering.md %}

## Armor Object
> GET /armor/:slug

Retrieves the armor object referenced by the slug.

## Attributes
**category** string

Describes a category of the armor object. Current categories are: 
* No Armor 
* Light Armor
* Medium Armor
* Heavy Armor
* Spell
* Class Feature
* Shield

**ac_string** string 

A description of the armor class (AC) that the armor object provides.

**strength_requirement** null or int

A numerical strength score required to don the armor.


**cost** string

A cost string in the form of "100 gp" that represents the suggested price for the armor.

**weight** string

An empty string.


**stealth_disadvantage** boolean

A value representing whether wearing the armor results in stealth disadvantage for the wearer.


### Standard Attributes
{% include_relative standard-attributes.md %}