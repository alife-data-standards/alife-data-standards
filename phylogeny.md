---
title: Phylogeny Standard
---

# Phylogeny Standard

A phylogeny depicts parent-child relationships of taxa over the course of evolution.
Phylogenies can be constructed for any taxonomic unit of organization (_e.g._,
individuals, genotypes, phenotypes, etc.).
We use the term taxa to refer generally to entities in a phylogeny.

**Navigation:**

<!-- TOC -->

- [Properties](#properties)
  - [Required Properties](#required-properties)
  - [Conventional Properties](#conventional-properties)
  - [Extra Properties](#extra-properties)
- [Example](#example)
- [Suggestions/Issues/Contributions](#suggestionsissuescontributions)

<!-- /TOC -->

## Properties

### Required Properties

These are the minimum set of properties (i.e., fields) required to specify a phylogeny.
You must have this information to conform to the standard.

- **id**: A unique identifier. Must be a non-negative integer.
  - There is a proposal to change this property name: [https://github.com/alife-data-standards/alife-data-standards/issues/16](https://github.com/alife-data-standards/alife-data-standards/issues/16)
- **ancestor_list**: A list of ids. These must correspond to other entities (entries) in the current file.
  They are assumed to refer to the most direct ancestor(s) of this entity that exist with in a file.
  In many cases, these will be the direct parent(s) of this entity, but this will not always be the case.

### **ancestor_list** Specification & Representation Details

If using a serialization format that supports first-class list representations within row columns (e.g., JSON), that representation should be used to serialize **ancestor_list** entries.

If using a serialization format without direct support for list representation within row columns (e.g., CSV), **ancestor_list** entries should be serialized as strings.
An **ancestor_list** string must open with a left square bracket (`[`) as its first character and close with a right square bracket (`[`) as its last character.
Between the brackets, **ancestor_list** entries should appear with sequential entries separated by a comma (`,`) character.
A single space character (` ` i.e., U+0020 SPACE/ASCII 32) may optionally follow each `,` separator.
As examples, the strings `[]`, `[1]`, `[1,2]`, and `[1, 2]` conform to **ancestor_list** requirements.

Trailing comma string representations (i.e., `[,]`, `[1,]`, `[1,2,]`, etc.) are not supported under this standard.
Leading zeros on integer identifiers are also not supported.

Note that RFC 4180 requires CSV fields containing comma `,` characters to be escaped with surrounding `"` characters.
Thus, `"[1, 2]"` would be a valid **ancestor_list**-column CSV field.
Under RFC 4180, fields that do not contain comma `,` characters should not be escaped.
Fields containing `[1]` or `[]` would be valid while fields containing `"[1]"` or `"[]"` would not.

For historical reasons, support should also be provided for `[None]`, `[none]`, or `[NONE]` as string representations of an empty ancestor list.
However, new data should not use this convention and instead represent an empty ancestor list with the string `[]`.

### Conventional Properties

These are common, but not required properties, for describing phylogenies.
If you have any of this information in your data, you should format it conventionally.

- **origin_time:** Time that this entity first came into existence (in whatever time units the system that generated this data uses).
- **destruction_time:** Time that this entry went out of existence (in whatever time units the system that generates this data uses).

### Extra Properties

Additional properties can always be added (as long as their names do not conflict with the names of existing properties).
Some tools may require specific additional properties to be present.
If it becomes apparent at any point that one of these properties is of use to a sizable portion of the community,
a discussion should be opened about adding it to the official list of conventional properties.

## Example

Below is a toy phylogenetic tree and a standard-compliant data table that specifies
the phylogeny, including required, conventional, and extra properties.

![example phylogeny](./media/toy-phylogeny.png)

## Suggestions/Issues/Contributions

The phylogeny standard is still under active discussion. Join in [here](https://github.com/alife-data-standards/alife-data-standards/issues?q=is%3Aissue+is%3Aopen+label%3Aphylogeny)!
