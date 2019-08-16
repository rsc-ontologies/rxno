# RXNO: reaction ontologies

RXNO is the name reaction ontology. It contains more than 500 classes representing organic reactions such as the Diels–Alder cyclization.

MOP is the molecular process ontology. It contains the underlying molecular processes, for example cyclization, methylation and demethylation.

Both ontologies are stored as .obo and .owl files, both of which can be read by Protege (http://protege.stanford.edu/).

You can browse the terms here: http://www.ebi.ac.uk/ols/ontologies/rxno and here: http://www.ebi.ac.uk/ols/ontologies/mop

## Steps for release

1. You will need to obtain a tool to convert OBO to OWL (or _vice versa_ if you're editing the OWL), for example ROBOT, which is available here: http://robot.obolibrary.org/
2. `java -jar robot.jar convert --input rsc-cmo/chmo.obo --output rsc-cmo/chmo.owl`
3. Check that the resulting file doesn't violate DL: `java -jar robot.jar validate-profile --input rsc-cmo/chmo.owl --profile DL --output rsc-cmo/dl.txt`

Colin Batchelor

2019-08-16
