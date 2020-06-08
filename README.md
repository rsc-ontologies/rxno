# RXNO: reaction ontologies

RXNO is the name reaction ontology. It contains more than 500 classes representing organic reactions such as the Diels–Alder cyclization.

MOP is the molecular process ontology. It contains the underlying molecular processes, for example cyclization, methylation and demethylation.

Both ontologies are stored as .obo and .owl files, both of which can be read by Protege (http://protege.stanford.edu/).

You can browse the terms here: http://www.ebi.ac.uk/ols/ontologies/rxno and here: http://www.ebi.ac.uk/ols/ontologies/mop

## Steps for release

1. You will need to obtain a tool to convert OBO to OWL (or _vice versa_ if you're editing the OWL), for example ROBOT, which is available here: http://robot.obolibrary.org/
2. `java -jar robot.jar convert --input rxno.obo --output rxno.owl`
3. `java -jar robot.jar convert --input mop.obo --output mop.owl`
4. (currently optional for various reasons) Check that the resulting files don't violate DL: `java -jar robot.jar validate-profile --input rxno.owl --profile DL --output dl.txt`
5. `java -jar robot.jar validate-profile --input mop.owl --profile DL --output dl.txt`

Colin Batchelor

2020-06-08
