# sib_riken_collabotation

List of SPARQL queries example for [RIKEN BioResource MetaDatabase](https://knowledge.brc.riken.jp/bioresource/)].

SPARQL endpoint: https://knowledge.brc.riken.jp/sparql

## List
### queryExample01.rq
#### 01 Get RIKEN BRC mice having Mammalian Phenotype Ontology (MP) terms.
prefix obo: <http://purl.obolibrary.org/obo/>
prefix brcanimal:<http://metadb.riken.jp/db/rikenbrc_mouse/>
prefix obo: <http://purl.obolibrary.org/obo/>
SELECT DISTINCT ?mouse
WHERE {
    ?mouse rdfs:subClassOf brcanimal:Strain.
	?mouse obo:RO_0002200 ?mp.
}
