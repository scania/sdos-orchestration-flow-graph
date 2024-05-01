# Orchestration Flow Graph

Graph which has instances of Orchestration Ontology. Orchestration ontology is a model with rules, options and restriction to create flow graphs.
Flow graph can be designed using Orchestration FlowGraph Designer([Orchestration FlowGraph Designer](https://github.com/scania/sdos-orchestration-flow-designer)).
The basic flow of a OFG is to start with a Task instance and have a relation to sequence of Actions. These Actions are connected to achieve the process of **E**xtract-**T**ransform-**L**oad.
It is recommended to have a single orchestration flow per flow graph.


## Orchestration ontology

ontology has different classes which serves different functionality.
* **Action class** is used to define the api call’s. It supports rest and soap api protocols. Parameters used for the api calls can be defined here.
* **Authentication method class** is used to define the authentication method for the api calls. it supports both basic auth and token approach.
* **Parameter class** is used to define the parameters through which the actions exchange the runtime data’s. It is also used to pass the value as user input.
* **Script class** is used to define the transformation logic for the flow. Groovy script transform the api response into knowledge graph.
* **Task class** is the entry point for the flow where it defines the parameters required to start the flow. Each action class instances are linked to form the flow and the flow continues until it finds there is no next Action
* **ResultMetaData** is used to define the metadata information in resultgraph, which will be used for Named Graph Security. (**Note** NamedGraph security is not included in this release)
* **System** is used to define the API domain system.
