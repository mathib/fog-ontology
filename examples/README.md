# Example ABox triples: application of FOG, OMG and GOM

This folder contains ABox RDF triples in Turtle (.ttl) format and [SPARQL-visualizer](https://github.com/MadsHolten/sparql-visualizer) demos (.json).

## 1) Basic dataset with two medieval columns
- Applied geometry schemas: PLY (ascii and binary), Collada, OBJ (with MTL), STEP, glTF (JSON and binary), E57, GEOM (RDF-based geometry)
- Describes: two columns and their respective parts (base-shaft-capital)
- Demonstrates: 
    - basic functionality of [OMG](https://w3id.org/omg#)/FOG for linking geometry descriptions to objects (e.g. buildings, storeys, building elements, etc.) using [OMG level of complexity 2](https://w3id.org/omg#description) (1 intermediate node between object and geometry description)
- files:
    - [`sample_abox_columns_dummy.ttl`](https://github.com/mathib/fog-ontology/blob/master/examples/sample_abox_columns_dummy.ttl): the RDF literals contain **dummy** geometry descriptions
	- [`sample_abox_columns.ttl`](https://github.com/mathib/fog-ontology/blob/master/examples/sample_abox_columns.ttl): the RDF literals embed or reference actual geometry descriptions
	- [`fog-demo.json`](https://github.com/mathib/fog-ontology/blob/master/examples/fog-demo.json): the content for [this SPARQL-visualizer demo](https://madsholten.github.io/sparql-visualizer/?file=https://raw.githubusercontent.com/mathib/fog-ontology/master/examples/fog-demo.json). It uses the content of the above `sample_abox_columns_dummy.ttl` file
	
## 2) Elaborated dataset related to the Saint Nicolas church
- Applied geometry schemas: PLY (binary, incl. textures), LAZ, PCD (ascii), DWG, SVG, OBJ, NXZ (Nexus), glTF (JSON)
- Describes: the medieval Saint Nicolas church in Ghent with a focus on the south nave
- Demonstrates: 
    - basic linking functionality of [OMG](https://w3id.org/omg#)/FOG using [OMG level of complexity 2](https://w3id.org/omg#description) (1 intermediate node between object and geometry description)
	- geometry metadata (grouping and derivation) using concepts from [OMG](https://w3id.org/omg#)
	- geometry metadata (coordinate systems, transformations, file size, geometry types) using concepts from [GOM](https://w3id.org/gom#)
- files:
    - [`sample_abox_snk_inspector.ttl`](https://github.com/mathib/fog-ontology/blob/master/examples/sample_abox_snk_inspector.ttl): This demonstrative dataset is created by a fictive monument inspector. The RDF literals embed or reference actual geometry descriptions
	- [`sample_abox_snk_contractor.ttl`](https://github.com/mathib/fog-ontology/blob/master/examples/sample_abox_snk_contractor.ttl): This demonstrative dataset is created by a fictive historic architecture research contractor. The RDF literals embed or reference actual geometry descriptions
