ReactionNetwork 
=================

* previously known as *Chemical Reaction Network*, but isn't necessarily about chemicals..
* contains compartments, which may contain species and reactions
* may be directed connections between species and reactions -> relationships like reactants, products, modifiers etc

create a ReactionNetwork 
--------------------------

TODO

export a ReactionNetwork 
--------------------------

* API contains functionality to export a /ReactionNetwork to different graph formats:
 * GraphML, e.g. to use it with [CytoscapeWeb](http://cytoscapeweb.cytoscape.org/) -- see also [Graphml Format Description](GraphmlFormatDescription)
 * DOT, e.g. to use it with GraphViz -- see also [Dot Format Description](DotFormatDescription)
 * JSON, e.g. to use it with [CytoscapeJS](http://cytoscape.github.io/cytoscape.js/) -- see also [Json Graph Format Description](JsonGraphFormatDescription)

[also see HierarchyNetwork](HierarchyNetwork)
