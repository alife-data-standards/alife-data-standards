# Genome Standard

## Required Fields

- **sequence** - A high percentage of genomes are, fundamentally, a sequence of something. More dicussion is required as to the exact format this field should take; we would like it to be able to accomodate genomes with more complicated structures, such as trees.

- **alphabet** - If a genome is a sequence, there must be some allowed set of characters in that sequence. The alphabet describes that. In some cases, it will be a simple list. For other genomes (e.g. genomes composed of doubles) it may not be possible to write every possible value.

## Conventional Fields

- **substitution matrix** - Many analyses that we might do on genomes depend on calculating distances between genomes. An easy default is to assume that all characters in the alphabet are equally similar to each other. In some circumstances, however, this will be inaccurate. In biology, this problem is handled with a substitution matrix: a table indicating the cost of substituting each element in the sequence for each other element (i.e. the dissimilarity between them).

# The genome standard is still under active discussion. Join in [here](https://github.com/alife-data-standards/alife-data-standards/issues?q=is%3Aissue+is%3Aopen+label%3Agenome)!
