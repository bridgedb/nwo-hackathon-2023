# Project 3: Nanomaterial ID mapping databases

* Lead: Egon Willighagen

## Description

## Participants

* Jeaphianne van Rijn

## Notes

* created a repo: https://github.com/bridgedb/create-nanomaterial-mappings
* two sources of ID mappings added
* NanoMILE <> ERM identifier mappings are now included
* JRC <> ERM identifiers
    * [notes from the first hackathon](https://docs.google.com/document/d/1v_RdqasghNU8el1aSOJEQrW_ixbpvAd9MlgU1shjTt4/edit?usp=sharing)
    * [previous tool](https://github.com/bridgedb/Wikidata2Bridgedb/blob/master/src/org/bridgedb/wikidata/Nanomaterials.java)
* Next step: [update datasources.tsv](https://github.com/bridgedb/datasources/pull/36) and make a BridgeDb release


## QC Results:

```
INFO: old database is create-nanomaterial-mappings 20230208 (build: 20230208)
INFO: new database is create-nanomaterial-mappings 20230208 (build: 20230208)
INFO: Number of ids in Nmerm (European Registry of Materials): 59 (unchanged)
INFO: Number of ids in Nmnm (NanoMILE): 58 (unchanged)
INFO: Number of ids in Nmjrc (Joint Research Center): 45 (unchanged)
INFO: Number of ids in Wd (Wikidata): 45 (unchanged)
INFO: new size is 2 Mb (changed +0.0%)
INFO: total number of identifiers is 207
INFO: total number of mappings is 207
NEW DB INFO: total number of primary ids in European Registry of Materials are 59
NEW DB INFO: total number of secondary ids in European Registry of Materials are 0
NEW DB INFO: total number of primary ids in NanoMILE are 58
NEW DB INFO: total number of secondary ids in NanoMILE are 0
NEW DB INFO: total number of primary ids in Joint Research Center are 45
NEW DB INFO: total number of secondary ids in Joint Research Center are 0
NEW DB INFO: total number of primary ids in Wikidata are 45
NEW DB INFO: total number of secondary ids in Wikidata are 0
OLD DB INFO: total number of primary ids in European Registry of Materials are 59
OLD DB INFO: total number of secondary ids in European Registry of Materials are 0
OLD DB INFO: total number of primary ids in NanoMILE are 58
OLD DB INFO: total number of secondary ids in NanoMILE are 0
OLD DB INFO: total number of primary ids in Joint Research Center are 45
OLD DB INFO: total number of secondary ids in Joint Research Center are 0
OLD DB INFO: total number of primary ids in Wikidata are 45
OLD DB INFO: total number of secondary ids in Wikidata are 0
```
