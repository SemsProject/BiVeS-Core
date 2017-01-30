Convert [MarkupDocuments](//MarkUp#MarkupDocument) to REPORTS in certain formats 
=================================================================================
/BiVeS knows some classes (extending [Typesetting](http://jdoc.sems.uni-rostock.de///BiVeS-Core/de/unirostock/sems/bives/markup/Typesetting.html)) able to convert format independent [MarkupDocuments](//MarkUp#MarkupDocument) into certain formats, such as [HTML](//TypeSetting#HTML) or [MarkDown](//TypeSetting#MarkDown)

HTML 
-----
* /src/main/java/de/unirostock/sems/bives/markup/TypesettingHTML.java ([JavaDoc](http://jdoc.sems.uni-rostock.de///BiVeS-Core/de/unirostock/sems/bives/markup/TypesettingHTML.html))
* HTML report looks like: /ReportHtml
* you can simply integrate it to your website
* plus some CSS rules to add some layout, see /ReportHtml

!MarkDown 
----------
* /src/main/java/de/unirostock/sems/bives/markup/TypesettingMarkDown.java ([JavaDoc](http://jdoc.sems.uni-rostock.de///BiVeS-Core/de/unirostock/sems/bives/markup/TypesettingMarkDown.html))
* learn more about [MarkDown](https://en.wikipedia.org/wiki/Markdown)
* exported !MarkDown looks like XXX
* convertable to serveral other formats -> convenient to integrate 

!Re/StructuredText 
-------------------
* /src/main/java/de/unirostock/sems/bives/markup/TypesettingReStructuredText.java ([JavaDoc](http://jdoc.sems.uni-rostock.de///BiVeS-Core/de/unirostock/sems/bives/markup/TypesettingReStructuredText.html))
* learn more about [Re/StructuredText](https://en.wikipedia.org/wiki///ReStructuredText)
* exported !Re/StructuredText looks like XXX
* convertable to serveral other formats -> convenient to integrate 

Add Your Own Report Layout 
---------------------------
* you need to extend /src/main/java/de/unirostock/sems/bives/markup/Typesetting.java ([JavaDoc](http://jdoc.sems.uni-rostock.de///BiVeS-Core/de/unirostock/sems/bives/markup/Typesetting.html))
* in [ markup] you'll get a [MarkupDocument](//MarkUp#MarkupDocument), TODO: document how to replace static stuff
* pass it to [None](A/P/I#GetaReport)