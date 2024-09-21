# DO-KB SPARQL queries

This repository contains SPARQL (version 1.1[^1]) queries designed for the Disease Ontology Knowledgebase (DO-KB) SPARQL sandbox (online editor) and endpoint (programmatic access/federated query endpoint) and utilize the data in the Human Disease Ontology (DO) ([disease-ontology.org](https://disease-ontology.org) / GitHub: [HumanDiseaseOntology](https://github.com/DiseaseOntology/HumanDiseaseOntology)).
- DO-KB SPARQL sandbox: https://disease-ontology.org/do-kb/sparql
- DO-KB SPARQL endpoint: https://sparql.disease-ontology.org/

Each query file has a metadata header (# commented YAML) followed by the SPARQL query. All metadata headers start with the following fields:
- **id:** A unique identifier in the format `DOq[0-9]{3}`.
- **description:** A brief description of what the query returns
- **input:** The source(s) that is/are queried.

Additional fields may also be included.

Additional information can be found on the [SPARQL resources](https://disease-ontology.org/do-kb/sparql_help) page of disease-ontology.org.

<details>

<summary><i>Code to list DO query IDs</i></summary>

```
grep -REoh "id: DOq[0-9]{3}" * | sort --reverse | uniq -c
```

</details>

[^1]: The SPARQL query language is designed "to query and manipulate RDF graph content on the Web or in an RDF store." Detailed information about SPARQL 1.1 is available from the W3C at https://www.w3.org/TR/2013/REC-sparql11-overview-20130321/.
