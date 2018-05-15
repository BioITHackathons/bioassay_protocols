# BioAssay Protocols

## Background

Assay protocols are publicly communicated using scientific English, which means that in the literature they are usually encountered as PDF files. This is quite possibly the least machine-readable format in common use, which severely limits the extent to which FAIR principles can be applied. The situation is only slightly better in public or private databases: the descriptive content is likely to abstracted into plain text (ASCII/unicode), and in some cases there is limited additional metadata. Private databases often use an _ad hoc_ set of drop-down lists or text fields for metadata, which is rarely standardized. The present situation is that published assay protocols can only be searched using crude keyword techniques, and most efforts to further markup a collection of protocols are done in mutually incompatible ways.

Extending FAIR principles to bioassay protocols requires that these *human-readable* documents be marked up with *machine-readable* metadata. The first resource that must be established is a dictionary (or multiple dictionaries that can be mapped to each other when they overlap). The most promising option seems to be ontologies that are part of the semantic web, such as:

* **BioAssay Ontology** (BAO)
* **Drug Target Ontology** (DTO)
* **Cell Line Ontology** (CLO)
* ... and others

Some examples of public bioassay protocol sources:

* **PubChem**: the assay collection is easily accessible interactively or by API, and provides some metadata, but most of it is noisy and lacks any kind of schema; the ingestion process includes data from essentially any source, and the quality varies between both extremes

* **PubMed**: a vast source of published papers, many of which contain assay protocols, but with limited information about where the content is located

* **ChEMBL**: a collection of human-curated assays with a small amount of very well defined metadata; unfortunately the text description of the assay is unavailable, and the metadata fields are not comprehensive

* **BARD**: an effort to add metadata to public content, which is unfortunately discontinued; the annotations were derived from the BioAssay Ontology, but not exactly the same

When metadata is available (and is both thorough and accurate), additional use cases include:

* searching (with 100% accuracy and precision)
* specific comparisons (internal & external data)
* bulk similarity comparisons & clustering
* ELN support: tagging, verification, completion, etc.
* automated alerts
* structure-activity data gathering
* ... and others

These capabilities affect all of the FAIR (Findable, Accessible, Interoperable, Reproducible) goals.

## Goals

Assume that assay data is already openly available in some form, whether it be raw text, PDF files, Word documents, or some mixture of text, figures and partial metadata. There are two objectives that must be achieved:

* Define a schema based on an open vocabulary
* Apply it consistently to assay documents

The vocabulary can be any open format, but semantic web options are already quite advanced: other possibilities should be discussed if applicable. The schema should provide some rules or guidelines as to how the vocabulary is applied to common types of assay protocols.

The schema needs to be applied to a large number of assay documents in order to be useful. There are two common approaches: _fully automated_ and _manual curation_, as well as some hybrid combinations. Fully automated methods (e.g. natural language processing) have the advantage of being immediately applicable to millions of documents, but they are typically very noisy. Manual curation methods produce very high quality data and facilitate searching that is essentially error free, but the process is expensive and slow. Another option is to identify data sources that have some existing metadata, and ensure that each option can be accurately mapped to the chosen schema.

By the end of the hackathon, we should have either consensus or several different candidates for vocabulary/schema options. We should have several examples of how to apply this schema to the example assay datasets. We should have several putative roadmaps for how to build a software tool that provides these annotations, by some strategy - whether it be automatic, manual and/or mapping - and some practical suggestions for how to go about applying it to the millions of assays that exist in the public space.

## Datasets

The following 4 protocols are available in the PubChem assays collection, and are diverse examples from 4 different laboratories:

1. [AID 1885](https://pubchem.ncbi.nlm.nih.gov/bioassay/1885): Luminescence Cell-Based/Microorganism Primary HTS to Identify Inhibitors of T.Cruzi Replication (primary assay, Broad Institute). [BAE](https://beta.bioassayexpress.com/assign.jsp?uniqueID=pubchemAID%3A1885)

2. [AID 624353](https://pubchem.ncbi.nlm.nih.gov/bioassay/624353): Fluorescence polarization-based biochemical dose-response assay for inhibitors of wild-type (WT) recombinant IDE (counterscreen, Scripps Institute). [BAE](https://beta.bioassayexpress.com/assign.jsp?uniqueID=pubchemAID%3A624353)

3. [AID 624023](https://pubchem.ncbi.nlm.nih.gov/bioassay/624023): QHTS For Inhibitors Of Mutant Isocitrate Dehydrogenase 1 (IDH1) (lead optimization, NCATS Chemical Genomics Center). [BAE](https://beta.bioassayexpress.com/assign.jsp?uniqueID=pubchemAID%3A624023)

4. [AID 1224875](https://pubchem.ncbi.nlm.nih.gov/bioassay/1224875): A CellTox Green Cytotoxicity Assay to monitor cytotoxicity in HEK293 cells (toxicity, EPA Tox21). [BAE](https://beta.bioassayexpress.com/assign.jsp?uniqueID=pubchemAID%3A1224875)
