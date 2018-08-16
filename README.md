## Overview

The Artificial Life (ALife) community is awash with disparate software systems,
many of which produce data about the same underlying processes. This results in
duplicated effort in developing analysis tools and visualizations. We believe we
can fix this problem by developing a community consensus around digital standards
for common data types (*e.g.*, genomes, phylogenies, etc.).
Our aim for these standards is for them to be useful to a wide range of artificial
life systems, including artificial chemistries, abstract ecologies, evolutionary
systems, and any other communities who express interest.

Eventually, this repository will hold a generally-accepted specification for
these standards, but much discussion is sill required to get to that point.
Currently, this repository contains proposed draft specifications for the standards
and exists primarily as a home for further discussion to finalize them.

## What are we trying to standardize?

Our goal is to specify standard ways of describing and storing particular types
of *data*. These standards do **not** describe methods for analyzing or working
with data. By agreeing on standard ways of describing and storing data, it will
become easier to share and make use of analysis tools and visualizations.

## A Living Standard

The ALife data standards should be a community effort, changing to conform to the
needs of our community. Anyone is encouraged file issues on this repository to make
suggestions for new standard data types, point out problems with existing standards,
*et cetera*. Pull requests to make changes to standard documentation or to add new
standards are also welcome.

Eventually, we should develop policies/templates for requesting/specifying standards.
Suggestions for this are welcome!

## Standard Data Types

- [Phylogeny](./phylogeny/)
- [Genome](./genome/)