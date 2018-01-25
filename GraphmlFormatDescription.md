Graphs encoded in GraphML 
==========================

* e.g. to pass them to [CytoscapeWeb](http://cytoscapeweb.cytoscape.org/)
* TODO: detailed description of the graph (what are these keys? subgraphs etc)
* see also [GraphML](https://en.wikipedia.org/wiki/GraphML)
* TODO: how to configure CytoscapeWeb (javascripts etc)
* TODO: demo
* example Graph:

```xml
<graphml>
	<key attr.name="name" attr.type="string" for="node" id="name"/>
	<key attr.name="node set" attr.type="string" for="node" id="ns">
			<default>species</default>
	</key>
	<key attr.name="version" attr.type="int" for="all" id="vers">
			<default>0</default>
	</key>
	<key attr.name="modifier" attr.type="string" for="edge" id="mod">
			<default>none</default>
	</key>
	<graph edgedefault="directed" id="G">
		<node id="c1">
			<data key="vers">0</data>
			<data key="name">compartment</data>
			<graph edgedefault="directed" id="G1">
				<node id="s2">
					<data key="ns">species</data>
					<data key="vers">0</data>
					<data key="name">sigb</data>
				</node>
				<node id="s1">
					<data key="ns">species</data>
					<data key="vers">0</data>
					<data key="name">lacz</data>
				</node>
				<node id="r3">
					<data key="ns">reaction</data>
					<data key="vers">2</data>
					<data key="name">sigb degr</data>
				</node>
				<!-- more nodes -->
			</graph>
		</node>
		<edge source="s2" target="r3">
			<data key="mod">none</data>
			<data key="vers">0</data>
		</edge>
		<edge source="s4" target="r3">
			<data key="mod">stimulator</data>
			<data key="vers">-1</data>
		</edge>
		<!-- more edges -->
	</graph>
</graphml>
```