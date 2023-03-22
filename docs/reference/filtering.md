---
layout: page
title: Filtering
---


# Filtering
Filtering lists in the open5e API uses [django-filter](https://django-filter.readthedocs.io/en/latest/index.html). This maps fields to lookups. The [list of lookups](https://docs.djangoproject.com/en/4.1/topics/db/queries/#field-lookups) is managed by django. Here is the set that you may see available within the API.

## Filters

**exact** An “exact” match. Default.
> GET /spells/?name=Amplify%20Gravity

**iexact** A case-insensitive match.
> GET /spells/?school__iexact=NeCrOmAnCy

**in** An exact match on ANY of the values. Comma-separated.
> GET /spells/?school__in=necromancy,evocation

**range** Range test (inclusive).
> GET /spells/?level_int__range=7,9

**contains** Case-sensitive containment test.
> GET /spells/?dnd_class__contains=Bard

**icontains** Case-insensitive containment test.
> GET /spells/?dnd_class__icontains=cLeRiC

### Filters not yet implemented in our API.

**lte,gte** Less than or equal to, or greater than or equal to, respectively.

**lt,gt** Less than or greater than.

**startswith, endswith** Starts-with and ends-with search, respectively.

**istartswith, iendswith** Case-insensitive starts-with and ends-with search.