---
layout: page
title: Documents
---

# Documents
This is an object representation of the documents added to the open5e-api database. Documents are a collection of 5e content. You can retrieve a document to see it's author, license, and copyright.

## Document List
> GET /documents

Retrieves a list of document objects.

### Filters
The following filtering options are available. When multiple filters are used, they are combined with AND logic.

| field | exact | iexact | in | range | icontains |
|---|---|---|---|---|---|
|  **title** | supported  | unsupported | unsupported | N/A | unsupported |
|  **document_slug** | supported  | unsupported | unsupported | N/A | unsupported |
|  **organization** | supported  | unsupported | unsupported | N/A | unsupported |
|  **license** | supported  | unsupported | unsupported | N/A | unsupported |

For more information on filtering, see the [Filtering] page.

### Ordering
{% include_relative standard-ordering.md %}

## Document Object
There is not an API request that retrieves a single document object.

## Attributes

**title** string
The title of the document.

**slug** string

A [slugified](https://docs.djangoproject.com/en/4.1/ref/utils/#django.utils.text.slugify) short name of the document. This is chosen upon import.

**url** string

A reference url for the document.

**license** string

A description of the license that the document was released under, such as "Open Gaming License" or "Creative Commons".

**desc** string

A description of the document itself.

**author** string

The full name of all authors of the document.

**organization** string

An empty string.

**version** string (major.minor)

A version number, in the format of "9.9" with just the major and minor version numbers.

**created_at** timestamp

The date in which the data was created in the open5e database. NOT the date of publication.

**copyright** string

The copyright string provided by the publishers of the document.

**license_url** string

"http://open5e.com/legal"