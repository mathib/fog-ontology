# The FOG ontology - File Ontology for Geometry formats

## HTML documentation and raw ontology per serialisation

* base URI: [https://w3id.org/fog#](https://mathib.github.io/fog-ontology/#)
* Canonical URI for the HTML representation: [https://w3id.org/fog/fog.html](https://mathib.github.io/fog-ontology/#)
* Canonical URI for the Turtle representation: [https://w3id.org/fog/fog.ttl](https://mathib.github.io/fog-ontology/ontology.ttl)
* Canonical URI for the n-triples representation: [https://w3id.org/fog/fog.nt](https://mathib.github.io/fog-ontology/ontology.nt)
* Canonical URI for the json-ld representation: [https://w3id.org/fog/fog.jsonld](https://mathib.github.io/fog-ontology/ontology.json)
* Canonical URI for the RDF/XML representation: [https://w3id.org/fog/fog.rdf](https://mathib.github.io/fog-ontology/ontology.xml)

The most recent version of FOG is always available in this Github repository

## Introduction to FOG

The File Ontology for Geometry formats (FOG) provides geometry schema specific relations between things (e.g. building objects) and their geometry descriptions. These geometry descriptions can be (1) RDF-based (e.g. using specific ontologies such as GEOM, OntoBREP, etc.), (2) RDF literals containing embedded geometry of existing geometry formats and (3) RDF literals containing a reference to an external geometry file. The FOG ontology extends the [Ontology for Managing Geometry (OMG)](https://w3id.org/omg#) and consists of two taxonomies of (sub)properties, one for RDF-based geometry schemas with as root object property the [omg:hasComplexGeometryDescription](https://w3id.org/omg#hasComplexGeometryDescription) and one for existing geometry schemas that can be represented using RDF literals with as root datatype property [omg:hasSimpleGeometryDescription](https://w3id.org/omg#hasSimpleGeometryDescription). This first series of properties (e.g. [fog:asGltf](https://w3id.org/fog#asGltf)) is then splitted per version of the geometry schema (e.g. [fog:asGltf_v2.0](https://mathib.github.io/fog-ontology/#asGltf_v2.0)), which are again splitted further if the geometry format consists of different kind of files (e.g. [fog:asGltf_v2.0-glb](https://mathib.github.io/fog-ontology/#asGltf_v2.0-glb)).

## Contributing to FOG

The FOG ontology is incomplete by nature, as it's impossible to contain all existing geometry schemas. If you notice that some geometry schemas are missing and you need them for your project, you can either create an issue in the [Github repository](https://github.com/mathib/fog-ontology), or you can fork it and submit a pull request.

## sparql-visualizer demo

An [online sparql-visualizer demo](https://madsholten.github.io/sparql-visualizer/?file=https://raw.githubusercontent.com/mathib/fog-ontology/master/examples/fog-demo.json) is available, containing sample Abox triples and example queries. The RDF literals in the Abox triples are dummies to make it more easily to visualize them as a graph. The same Abox triples with the full RDF literals are also available in this repository in [`examples/sample_abox_columns.ttl`](https://github.com/mathib/fog-ontology/blob/master/examples/sample_abox_columns.ttl).

## Contributors

[Mathias Bonduel](https://github.com/mathib) - KU Leuven

[Anna Wagner](https://github.com/AnnaWagner) - TU Darmstadt

[Pieter Pauwels](https://github.com/pipauwel) - UGent

## References
Please cite the following paper when using FOG:

* Bonduel, M., Wagner, A., Pauwels, P., Vergauwen, M., & Klein, R. (2019). Including Widespread Geometry Formats in Semantic Graphs Using RDF Literals. In *Proceedings of the European Conference on Computing in Construction (EC3 2019)*. Chania, Greece.

The FOG ontology module extends OMG (Ontology for Managing Geometry), documented in the following paper:

* Wagner, A., Bonduel, M., Pauwels, P. & Rüppel, U. (2019). Relating Geometry Descriptions to its Derivatives on the Web. In *Proceedings of the European Conference on Computing in Construction (EC3 2019)*. Chania, Greece.