API 
====

BiVeS provides a sophisticated API, see [API package](https://github.com/SemsProject/BiVeS-Core/blob/master/src/main/java/de/unirostock/sems/bives/api)

API for Comparison of two Documents 
------------------------------------

 * super class (abstract): `/src/main/java/de/unirostock/sems/bives/api/Diff.java` ([JavaDoc](http://jdoc.sems.uni-rostock.de///BiVeS-Core/de/unirostock/sems/bives/api/Diff.html))
 * compare two XML files: `/src/main/java/de/unirostock/sems/bives/api/RegularDiff.java` ([JavaDoc](http://jdoc.sems.uni-rostock.de///BiVeS-Core/de/unirostock/sems/bives/api/RegularDiff.html))
 * bives-cellml:wiki also provides specialized API two compare two CellML files:  ([JavaDoc](http://jdoc.sems.uni-rostock.de///BiVeS-CellM/L/de/unirostock/sems/bives/cellml/api/CellMLDiff.html))
 * bives-sbml:wiki also provides specialized API two compare two SBML files:  ([JavaDoc](http://jdoc.sems.uni-rostock.de///BiVeS-SBML/de/unirostock/sems/bives/sbml/api/SBMLDiff.html))

Compare two versions
--------------------

### Get a Report 
* different formats:
 * HTML report: 
 * own format: [getReport](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/api/Diff.html#getReport(de.unirostock.sems.bives.markup.Typesetting)), provide an instance of your own  [Typesetting class](https://github.com/SemsProject/BiVeS-Core/blob/master/src/main/java/de/unirostock/sems/bives/markup/Typesetting.java) class. (see [TypeSetting](TypeSetting#add-your-own-report-layout))

### Get a Graph 
* different formats:
 * GraphML: see [Graphml Format Description](GraphmlFormatDescription)
 * JSON: see [Json Graph Format Description](JsonGraphFormatDescription)
 * DOT: see [Dot Format Description](DotFormatDescription)

API for Information about a Single Document 
--------------------------------------------

* TODO
