# PGCDO: Prokaryotic Genomic Contents Definition Ontology

In comparative genomics, sometimes, expectations are expressed, about
the contents of a genome in given groups of organims (e.g. based on their
taxonomy, phenotype or habitat).

Enabling the description and verification of such expectations requires to
define exactly the genomic contents.
The Prokaryotic Genomic Contents Definition Ontology is a framework which
enables such definitions.
In particular, it defines \textit{genomic attributes} as measurable/observable
quantities in a genome. Thereby, it
differentiates the object of a measurement (called here
\textit{genomic content unit} and other variables of the required
measurement itself (such as the \textit{measurement mode} and \textit{measurement
region}).

## Ontology files

The ontology is defined using the OBO format and consists of a single file
(``pgcdo.obo``).

## Structure and contents

The ontology consists of the four parts, defining genomic attributes,
genomic region types, modes of measurement and genomic content units.

### Genomic attributes

The first part defines genomic attributes (currently, only the definition of
genomic attribute itself belongs to it). A genomic attribute is defined
as a measurable
value derived from the observation, a computation or a prediction of some
aspects the genome (called genomic content unit, see below).

Besides the genomic content unit, more elements belong to the definition of
a genomic attribute, such as the region of the genome taken into consideration,
as the mode of measurement.

### Genomic regions

The second part of the ontology consists of the definition of genomic region
and the subtree under it, in which each node belongs to the namespace
``genomic_region_type``.

A genomic region is required in the concrete definition of a genomic attribute
(i.e. in a instance of A0001, genomic\_attribute) and will belong to one
of the given types of genomic regions.

Genomic regions of different type are for instance specific molecules,
or all molecules of a given type, such as chromosomes or plasmids.

### Measurement modes

The third part of the ontology consists of the definition of measurement mode,
and of the different measurement modes, in the namespace ``measurement_mode``.

The same genomic content unit can be considered under different aspects,
depending on the measurement mode, giving rise to a different values.
Different modes are e.g. the absolute count, relative frequency,
presence/absence and total or average sequence length (e.g. total
length of the coding sequences), or number of subunits
(e.g. number of exons in some kind of genes).

### Genomic content unit

The definition of unit of genomic content is given in the fourth part of
the ontology. It is followed by different categories of genomic content
units (sequence and annotation based), belonging to the namespace
``genomic_content_unit_type_category``.

Genomic content unit types are then given as part of the namespace
``genomic_content_unit_type``. Not all possible genomic content unit types
are given, in particular not those under the node ``feature``,
as these are rather better
defined by a link to a term of the sequence ontology (SO).

## Adding new terms to the ontology

If measurement modes, genomic region types or genomic content unit types (or
even genomic content unit type categories) are necessary, a pull request can
be sent.

## Acknowledgements

This ontology has been created in context of the
DFG project GO 3192/1-1 “Automated
characterization of microbial genomes and metagenomes by collection and
verification of association rules”. The funders had no role in
study design, data collection
and analysis.
