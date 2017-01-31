Graphs encoded in DOT 
======================

* e.g. to convert them to static images using GraphViz
* see also [DOT](https://en.wikipedia.org/wiki/DOT_language)
* TODO: detailed description of the graph
* TODO: how to run graphviz (neato, dot etc.. differences? different examples)
* TODO: demo
* example Graph:

```dot
digraph BiVeSexport {
	graph [overlap=false];
	edge [len=1.3];
	node [fontsize=11];
	subgraph clusterc1 {
		label = "compartment";
		color=lightgrey;
		s2[label="sigb",shape=circle];
		s1[label="lacz",shape=circle];
		s4[label="x",shape=circle];
		s3[label="IPTG",shape=circle];
		r3[label="sigb degr",color=yellow,shape=diamond];
		r2[label="lacz degr",shape=diamond];
		r1[label="sigb syn",color=yellow,shape=diamond];
		r4[label="x syn",color=yellow,shape=diamond];
		r5[label="lacz syn",color=yellow,shape=diamond];
	}
	s2->r3;
	s4->r3[color=red,style=dashed,arrowType=normal];
	s4->r3[color=blue,style=dashed,arrowType=odot];
	s1->r2;
	r1->s2;
	s3->r1[color=red,style=dashed,arrowType=normal];
	s3->r1[color=blue,style=dashed,arrowType=odot];
	r4->s4;
	s2->r4[color=red,style=dashed,arrowType=normal];
	s2->r4[color=blue,style=dashed,arrowType=odot];
	r5->s1;
	s2->r5[color=red,style=dashed,arrowType=normal];
	s2->r5[color=blue,style=dashed,arrowType=odot];
	label="Diff Graph created by BiVeS";
}
```
