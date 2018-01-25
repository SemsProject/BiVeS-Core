HierarchyNetwork 
==================

* representing a graphical hierarchy network, intended to visualize CellML hierarchical dependencies of components
* contains components which may contain variables
* there may be directed connections from parent components to child components representing the hierarchy among components
* variables can be connected visualizing the flow of information between them

create a /HierarchyNetwork 
---------------------------

TODO

export a /HierarchyNetwork 
---------------------------

* API contains functionality to export a HierarchyNetwork to different graph formats:
  * GraphML, e.g. to use it with [CytoscapeWeb](http://cytoscapeweb.cytoscape.org/) -- see also /GraphmlFormatDescription
  * DOT, e.g. to use it with GraphViz -- see also DotFormatDescription
  * JSON, e.g. to use it with [CytoscapeJS](http://cytoscape.github.io/cytoscape.js/) -- see also /JsonGraphFormatDescription

Modifications 
--------------

* a /HierarchyNetworkComponent may report following modifications:
  * /GraphEntity.MODIFIED: properties of this component have changed, or its parental association in the corresponding hierarchy was modified.
  * /GraphEntity.INSERT: this component wasn't present in the original document, but was inserted in the modified version
  * /GraphEntity.DELETE: this component isn't present in the modified version, while it was present in the original document
  * /GraphEntity.UNMODIFIED: component and its parental association in the component hierarchy hasn't changed (variables in this component may have been inserted/deleted/modified)
* a /HierarchyNetworkVariable may report following modifications:
  * /GraphEntity.MODIFIED: its label has changed, or some other properties were modified
  * /GraphEntity.INSERT: it wasn't present in the original document
  * /GraphEntity.DELETE: it isn't present in the modified document anymore
  * /GraphEntity.UNMODIFIED: same properties in both the original and the modified document

[also see ReactionNetwork](ReactionNetwork)