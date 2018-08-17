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

## A living standard

The ALife data standards should be a community effort, changing to conform to the
needs of our community. Anyone is encouraged file issues on this repository to make
suggestions for new standard data types, point out problems with existing standards,
*et cetera*. Pull requests to make changes to standard documentation or to add new
standards are also welcome.

Eventually, we should develop policies/templates for requesting/specifying standards.
Suggestions for this are welcome!

## Standard data types

- [Phylogeny](./phylogeny.md)
- [Genome](./genome.md)

## Organization

Standards-related materials all live inside repositories owned by the alife-data-standards organization. These materials are divided into two groups:

- The standards themselves, which live in this repository. Changes to the standards can be proposed in three different ways (to accommodate different levels of comfort with GitHub): submitting a pull request with the proposed changes to this repository, making an issue on this repository, or e-mailing the standards maintainers (listed below). Once a modification is proposed, discussion on it will take place via GitHub issues (which also supports contributions via e-mail). When consensus is reached, the change will be added to the official standards.
- A vetted collection of tools that work with standards-compliant data, which live in the tools repository. These tools include converters into and out of the standards format. If you have written a tool that you would like to add to this repository, you can request that it be added via pull request, issue, or an e-mail to the maintainers. The maintainers will then confirm that the tool works with the current version of the standards before accepting the addition. Updates to tools can be added in the same way. This repository also houses a list of third-party tools that work with data in standards format. These tools are not vetted or tested by the ALife Data Standards maintainers. You can request that a tool be added to this list with a pull request, GitHub issue or e-mail.

### Current maintainers

- [Cliff Bohm](http://www.cliffbohm.weebly.com) (cliff.bohm@gmail.com)
- [Alexander Lalejini](http://www.lalejini.com) (amlalejini@gmail.com)
- [Emily Dolson](http://www.emilyldolson.com) (EmilyLDolson@gmail.com)
