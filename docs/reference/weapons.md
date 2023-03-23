---
layout: page
title: Weapons
---

# Weapons
This is an object representation of the weapon items added to the open5e-api database. You can retrieve weapons to see cost, weight, and other data points.

## Weapon List
> GET /weapons

Retrieves a list of weapon objects.

### Filters
The following filtering options are available. When multiple filters are used, they are combined with AND logic.

| field | exact | iexact | in | range | icontains |
|---|---|---|---|---|---|
|  **name** | supported  | unsupported | unsupported | N/A | unsupported |
|  **document_slug** | supported  | unsupported | unsupported | N/A | unsupported |

For more information on filtering, see the [Filtering] page.

### Ordering
{% include_relative standard-ordering.md %}

## Weapon Object
> GET /weapon/:slug

Retrieves the weapon object referenced by the slug.

## Attributes
**category** string

Describes a category of the weapon object. Current categories are: 
* Simple Melee Weapons
* Simple Ranged Weapons
* Martial Melee Weapons
* Martial Ranged Weapons

**damage_dice** string 

A description of the armor class (AC) that the armor object provides.

**damage_type** string
One of the following types of damage:
* bludgeoning
* piercing
* slashing

**cost** string

A cost string in the form of "100 gp" that represents the suggested price for the weapon.

**weight** string

A string describing the weight of the weapon.

**properties** string list

A list of various properties that apply to the weapon.

### Standard Attributes
{% include_relative standard-attributes.md %}