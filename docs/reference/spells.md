---
layout: page
title: Spells
---

# Spells
This is an object representation of the spells added to the open5e-api database. You can retrieve spells to see components, range, level, and other data points.

## Spells List
> GET /spells

Retrieves a list of spell objects.

### Filters
The following filtering options are available. When multiple filters are used, they are combined with AND logic.

| field | exact | iexact | in | range | icontains |
|---|---|---|---|---|---|
|  **name** | supported  | supported | unsupported | N/A | unsupported |
|  **slug** | supported  | supported | supported | N/A | unsupported |
| **level**  | supported  | supported | supported | N/A | unsupported |
| **level_int**  | supported  | supported | unsupported | supported | N/A |
| **school**  | supported  | supported | supported | N/A | unsupported |
| **duration**  | supported  | supported | supported | N/A | unsupported |
| **components**  | supported  | supported | supported | N/A | unsupported |
| **concentration**  | supported  | supported | supported | N/A | unsupported |
| **casting_time**  | supported  | supported | supported | N/A | unsupported |
| **dnd_class**  | supported  | supported | supported | N/A | supported |
|  **document_slug** | supported  | supported | supported | N/A | unsupported |

For more information on filtering, see the [Filtering] page.

### Ordering
{% include_relative standard-ordering.md %}

## Spell Object
> GET /spells/:slug

Retrieves the spell object referenced by the slug.

## Attributes
**desc** string

A description of the effects of the spell.

**higher_level** string

A description of what happens when casting the spell at a higher level.
 
**page** string

The page number from the original document that the spell is on.


**range** string

A description of the range of the spell.

**components** string

Any number of "V", "S", "M" representing the components required to cast the spell.
"M",
    
**material**: "string

A description of the material components required.

**ritual** string

"yes" or "no" based on whether or not a ritual is required.
            
**duration** string

A description of the duration such as "instantaneous" or "Up to 1 minute"

**concentration** string

"yes" or "no" based on whether the spell requires concentration.


**casting_time** string

Amount of time to cast the spell, such as "1 bonus action" or "4 hours".
            
            
**level** string

String description of the level of the spell, such as "4th-level"

**level_int** int

An integer of the level. 0 is for cantrip.

**school** string

A string representation of the school of magic, such as "illusion" or "evocation".

**dnd_class** string

A comma separated list of classes that can learn this spell.

**archetype**

An empty string or the archetype that can learn this spell. If empty, you can assume all archetypes of the classes can learn it.


### Standard Attributes
{% include_relative standard-attributes.md %}