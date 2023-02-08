# Project 5: Visualizing derby databases

* Lead: Tooba Abbassi-Daloii

## Description
The BridgeDb project is collecting data to create secondary to primary mapping databases for [HGNC](https://www.genenames.org/), [UniProt](https://www.uniprot.org/), [HMDB](https://hmdb.ca/), [ChEBI](https://www.ebi.ac.uk/chebi/) and [Wikidata](https://www.wikidata.org/wiki/).
Scripts can be found [here](https://github.com/tabbassidaloii/create-bridgedb-secondary2primary/tree/main/src/).

## Problem

The secondary to primary mapping file for HGNC contains incorrect mappings. To visualize the issue, visualization tools were attempted, but the correct drivers couldn't be defined using DBeaver.

## Participants

* [Ammar](https://github.com/ammar257ammar)

## Solution

The problem was solved by decompressing the BridgeDB derby files, as explained [here](https://github.com/bridgedb/nwo-hackathon-2023/issues/5#issuecomment-1422416092) 


