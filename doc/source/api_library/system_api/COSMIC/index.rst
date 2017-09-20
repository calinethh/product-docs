COSMIC System API
!!!!!!!!!!!!!!!!!!!!!

COSMIC is the most comprehensive resource for exploring the impact of somatic mutations in human cancer.

Connection instructions:
Stored here as soon as we make the docs private.

Methods and Requirements

* This must be written as a REST API
* This must follow the format and standards defined in the existing API templates located here: https://bitbucket.org/snippetmd/snippet-api-platform
* All code must be documented. We use readthedocs for our documentation, so your documentation may be in sphinx/markdown language or plain text. See more about the documentation here: http://docs.readthedocs.io/en/latest/getting_started.html


**Data Inputs**
@@@@@@@@@@@@@@@

The input data should be assumed to be in a GA4GH-compatible format unless files are uploaded directly. If any new fields are added for inputs and outputs, their format should be matched as closely as possible to the GA4GH schema and they should be noted here. 


**Required**

HGVS ID: For large genes, might need to use HUGO symbol followed by sequence variation nomenclature eg. POLD1 R343H.
eg. rs140539427 is a mutation in POLD1 gene resulting in change in amino acid change. This potentially have a few HGVS ID: POLD1 c.1028G>A / POLD1 1028G>A / POLD1 p.R343H / POLD1 R343H etc.

Gene ID: To query the COSMIC database, the Ensembl Gene ID should be used. The Ensembl ID will come from the Ensembl database/API and will start with the characters "ENS" - for example, "ENSG00000012048"


**Data Outputs**
@@@@@@@@@@@@@@@@


**Required**

* Overview: Drug sensitivity data - these are the drugs the mutation will be sensitive to
* Drug resistance: This section shows the drugs that have been used to treat mutant tumours for the gene of interest. In related fields you can see any other genes that have been treated with the same drug(s), and the distribution of mutations that occur in those genes.
* FATHMM prediction: Prediction types - pathogenic (score 0.99) eg POLD1 R343H; neutral (score 0.07) eg BRCA2 p.L2136V

