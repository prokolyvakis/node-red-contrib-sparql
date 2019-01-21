SPARQL NodeRED Node
=============================

A Node-RED node that allows for the execution of SPARQL queries.


Install
-------
To install - change to your Node-RED user directory, which typically is:

`cd ~/.node-red/node_modules`

and copy-paste the `node-red-contrib-sparql` inside it!

Or

`sudo npm install prokolyvakis/node-red-contrib-sparql --save`


Usage
-----

The endpoint block is used to set the SPARQL endpoint on which the query will be performed.

For example, it can be set to:
 `http://dbpedia.org/sparql`

The query block is where the query should actually be written.

An example of a SPARQL query to the SPARQL endpoint mentioned above is the following:

```
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
SELECT ?label
WHERE { <http://dbpedia.org/resource/Asturias> rdfs:label ?label }
```

By convention, the result of the query will be stored on: 
`msg['payload']`



