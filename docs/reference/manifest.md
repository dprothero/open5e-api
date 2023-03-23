---
layout: page
title: Manifest
---

# Manifest
This is a special object representation of the files used to populate the open5e-api database. You can retrieve filename, type, and hash. It is meant to be queried to determine if a local file matches a file hosted on the server.

## Armor List
> GET /manifest

Retrieves a list of manifests.

### Filters
There are no filters available on this endpoint.

### Ordering
{% include_relative standard-ordering.md %}

## Manifest Object

## Attributes
**filename** string

The name of the file that was imported.

**type** string 

The type of data within the file (this is determined based on filename).

**hash** string md5

The md5 hash of the file's contents.

**created_at** timestamp

The time in which the file was loaded into the API.
