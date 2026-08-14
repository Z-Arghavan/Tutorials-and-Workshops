# on SKOS: Simple Knowledge Organization System

## What SKOS is for

SKOS is a lightweight W3C vocabulary for organising and aligning terminology. It is suitable for dictionaries, taxonomies, thesauri and classification systems.

## Core elements

| SKOS element | Purpose |
|---|---|
| `skos:Concept` | A term or concept |
| `skos:ConceptScheme` | The dictionary or concept system |
| `skos:prefLabel` | Preferred label in a language |
| `skos:altLabel` | Synonym or alternative label |
| `skos:definition` | Human-readable definition |
| `skos:broader` / `skos:narrower` | Informal hierarchical relationships |
| `skos:related` | Non-hierarchical association |
| `skos:Collection` | Group of related concepts |
| `skos:notation` | Classification code or identifier |

## Mapping between vocabularies

- `skos:exactMatch`: concepts are interchangeable across schemes.
- `skos:closeMatch`: concepts are similar but not necessarily identical.
- `skos:broadMatch`: the external concept is broader.
- `skos:narrowMatch`: the external concept is narrower.
- `skos:relatedMatch`: the concepts are associated.

Identical labels do not necessarily indicate identical meanings.

## SKOS versus RDFS and SHACL

```turtle
ex:Building skos:broader ex:Structure .
```

This means that *Building* is a narrower concept than *Structure*.

```turtle
ex:Building rdfs:subClassOf ex:Structure .
```

This formally means that every instance of `Building` is also an instance of `Structure`.

- **SKOS** is helpful to organise terminology and meanings.
- **RDFS or OWL** is helpful to represent formal domain structure.
- **DCTERMS, PROV-O and related vocabularies** are helpful for provenance and governance metadata.

## SKOS can be used for:

- multilingual labels and definitions;
- synonyms and alternative terminology;
- broader, narrower and related concepts;
- mappings between built-environment vocabularies;
- whether a resource is actually an ontology, dictionary, taxonomy or mixed semantic resource;
- support for LLM query expansion and GraphRAG retrieval.

## Main point

Not every semantic resource needs to be a formal ontology. The modelling language should match the purpose of the resource. SKOS supports shared terminology, while RDFS, OWL and SHACL provide stronger formal structures and constraints.

## Examples with DOR ontology

```turtle
dor:ReusePotential
    a owl:Class ;
    rdfs:label "Reuse Potential"@en ;
    skos:prefLabel "Reuse potential"@en .
```
```turtle
dor:ReusePotential
    skos:prefLabel "Reuse potential"@en ;
    skos:altLabel "Potential for direct reuse"@en .
```

```turtle
dor:ReusePotential
    skos:prefLabel "Reuse potential"@en ;
    skos:definition
        "The potential of a component or assembly to be reused without major intervention."@en .
```

```turtle
ex:BuildingTerm
    a skos:Concept ;
    skos:prefLabel "Building"@en ;
    skos:broader ex:BuiltAssetTerm .
```
