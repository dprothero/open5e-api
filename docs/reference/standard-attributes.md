All content types in the open5e-api database have the following standard attributes.

**name** string

A basic name of the content item.

**slug** string

A [slugified](https://docs.djangoproject.com/en/4.1/ref/utils/#django.utils.text.slugify) version of the name.

* In some scenarios, object slugs would conflict. In general, we append a short suffix based on the document origin slug of the later addition, such as **aboleth** and **aboleth-a5e**.

**document__slug** string
A slug that refers to a [Document]. This document is the source of this content item.

**document__title**
The title of the document referred to by the slug.

**document__license_url**
A url that links to a license for the document.