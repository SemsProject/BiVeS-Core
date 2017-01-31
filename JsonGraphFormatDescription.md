Graphs encoded in JSON 
=======================

* e.g. to pass them to [CytoscapeJS](http://cytoscape.github.io/cytoscape.js/)
* TODO: detailed description of the graph
* TODO: how to configure CytoscapeJS (stylesheet, javascripts)
* TODO: demo
* example Graph:

```json
{
	"elements": {
		"edges": [
			{
				"classes": "bives-ioedge",
				"data": {
					"source": "s2",
					"target": "r3"
				}
			},
			{
				"classes": "bives-stimulator bives-deleted",
				"data": {
					"source": "s4",
					"target": "r3"
				}
			},
			/* [...] */
		],
		"nodes": [
			{
				"classes": "compartment",
				"data": {
					"id": "c1",
					"name": "compartment"
				}
			},
			{
				"classes": "species",
				"data": {
					"id": "s2",
					"name": "sigb",
					"parent": "c1"
				}
			},
			{
				"classes": "reaction bives-modified",
				"data": {
					"id": "r3",
					"name": "sigb degr",
					"parent": "c1"
				}
			},
			/* [...] */
		]
	}
}
```
