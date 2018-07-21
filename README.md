# Wikidata Literature Summary

This repository contains a collection of Wikidata SPARQL queries to summarize a corpus of literature.
The corpus you wish to summarize is given in the `pmids.txt` file and is basically a list of quoted
PubMed identifiers:

```
"10024875"
"10025409"
"10051604"
"10051637"
"10053004"
```

The queries are given in `.template` files which have an essential `# PMIDS` line which is replaced
by the corpus, after which `curl` is used to execture the resulting SPARQL query, saving the results
in a matching `.csv` file:

```(bash)
make
```
