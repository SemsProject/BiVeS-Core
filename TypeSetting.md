Convert [MarkupDocuments](MarkUp#imarkup-document) to REPORTS in certain formats 
=================================================================================

BiVeS knows some classes (extending [Typesetting](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/Typesetting.html)) able to convert format independent [MarkupDocuments](MarkUp#markup-document) into certain formats, such as [HTML](TypeSetting#html) or [MarkDown](TypeSetting#mark-down)

HTML 
-----

* `/src/main/java/de/unirostock/sems/bives/markup/TypesettingHTML.java` ([JavaDoc](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/TypesettingHTML.html))
* HTML report looks like: [ReportHtml](ReportHTML)
* you can simply integrate it to your website
* plus some CSS rules to add some layout

MarkDown 
----------

* `/src/main/java/de/unirostock/sems/bives/markup/TypesettingMarkDown.java` ([JavaDoc](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/TypesettingMarkDown.html))
* learn more about [MarkDown](https://en.wikipedia.org/wiki/Markdown)
* exported MarkDown looks like XXX
* convertable to serveral other formats -> convenient to integrate 

Re/StructuredText 
-------------------

* `/src/main/java/de/unirostock/sems/bives/markup/TypesettingReStructuredText.java` ([JavaDoc](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/TypesettingReStructuredText.html))
* learn more about [Re/StructuredText](https://en.wikipedia.org/wiki/ReStructuredText)
* exported !Re/StructuredText looks like XXX
* convertable to serveral other formats -> convenient to integrate 

Add Your Own Report Layout 
---------------------------

* you need to extend `/src/main/java/de/unirostock/sems/bives/markup/Typesetting.java` ([JavaDoc](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/Typesetting.html))
* in `markup` you'll get a [MarkupDocument](MarkUp#markup-document), TODO: document how to replace static stuff
* pass it to [Get a Report](API#get-a-report)
