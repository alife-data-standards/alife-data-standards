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
- **ancestor_list**: A list of ids. These must correspond to other entities (entries) in the current file.
  They are assumed to refer to the most direct ancestor(s) of this entity that exist with in a file.
  In many cases, these will be the direct parent(s) of this entity, but this will not always be the case. <br/> 
  *Special values:*
    - "['none']" - Indicates that the taxon had no ancestor, and was either generated from scratch or introduced to the system via other means.

### Conventional Properties

These are common, but not required properties, for describing phylogenies.
If you have any of this information in your data, you should format it conventionally.

- **origin_time:** Time that this entity first came into existence (in whatever time units the system that generated this data uses). <br/>
- **destruction_time:** Time that this entry went out of existence (in whatever time units the system that generates this data uses). <br/>
  *Special values:*
    - 'none' - Indicates that the taxon was extant at the time of sampling.
### Extra Properties

Additional properties can always be added (as long as their names do not conflict with the names of existing properties).
Some tools may require specific additional properties to be present.
If it becomes apparent at any point that one of these properties is of use to a sizable portion of the community,
a discussion should be opened about adding it to the official list of conventional properties.

## Example

Below is a toy phylogenetic tree and a standard-compliant data table that specifies
the phylogeny, including required, conventional, and extra properties.

![example phylogeny](./media/toy-phylogeny.png)

## File Formats

Currently, two file formats are explicitly supported by the standard: comma-separated values (CSV) and [Javascript Object Notation (JSON)](https://www.json.org/). The details of describing a phylogeny using both file formats are given below.

### Comma-Separated Values (CSV)
**Organization**

For a .csv file to be standards-compliant, the first row is expected to contain a header that defines the properties of the entities.
Each entity (one specific taxon) of the phylogeny will fill one row of the .csv file. 

**Lists**

Lists of data in the .csv (*e.g.*, ancestor\_list) have their own syntax rules. 
A list is denoted by a pair of square braces surrounded by double quotes "[ ]". 
Each element in the list should be treated as a string, so it must be surrounded by its own pair of single quotes (*e.g.*, "['1','2']").

*List examples:*

    - Child of 123 in an asexual phylogeny: "['123']" 
    - Child of 123 and 456 in a sexual phylogeny: "['123', '456']"
    - Taxon with no ancestors: "['none']"

The list syntax is bulky but necessary. The outer quotation marks tell the parser to treat the contents as a string and thus inner commas are ignored. The brackets denote that the string is in fact a list. Single quotes around each element tell the parser to treat each element as a string, which we do for arbitrary precision and also for special values (*e.g.*, none).

While ancestor\_list is the only standards-defined property that is a list, any extra properties that are lists are required to use the same quoted bracket format.

**Example**
  
[CSV of example phylogeny (pictured above)](./examples/phylogeny_toy_csv.csv)


### Javascript Object Notation (JSON)


## Suggestions/Issues/Contributions

The phylogeny standard is still under active discussion. Join in [here](https://github.com/alife-data-standards/alife-data-standards/issues?q=is%3Aissue+is%3Aopen+label%3Aphylogeny)!
