---
title: Phylogeny Standard
---

# Phylogeny Standard

A phylogeny is a tree that describes ancestor-descendant relationships in a collection
of individuals.

## Required Fields

These are the minimum set of fields required to specify a phylogeny. You must have
this information to conform to the standard.

- **id**: A unique identifier. Must be a non-negative integer.
- **ancestor_list**: A list of ids. These must correspond to other entries in the current file. They are assumed to refer to the most direct ancestor(s) of this entry that exist with in a file. In many cases, these will be the direct parent(s) of this entry, but this will not always be the case.

## Optional Fields with Naming Conventions

These are common, but not required fields, for describing phylogeny. If you
have any of this information in your data, you should format it according to the conventions.

- **origin_time:** Time that this entry first came into existance (in whatever time units the system that generated this data uses).
- **destruction_time:** Time that this entry went out of existance (in whatever time units the system that generates this data uses).

## Additional Data

Additional fields can always be added (as long as their names do not conflict with the names of existing fields). Some tools may require specific additional fields to be present. If it becomes apparent at any point that one of these fields is of use to a sizable portion of the community, a discussion should be opened about adding it to the official list of optional fields with naming conventions.

# The phylogeny standard is still under active discussion. Join in [here](https://github.com/alife-data-standards/alife-data-standards/issues?q=is%3Aissue+is%3Aopen+label%3Aphylogeny)!
