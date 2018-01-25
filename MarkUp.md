Format-Independent Make-Up for reports 
=========================================

abstract mark up stuff to generate reports

MarkUp Interface 
------------------

* used to markup certain atomic objects (which for example represent formulars/units/quantities etc.)
* to add report independent markup use static methods in [MarkupDocument](#markup-document)
* see [/src/main/java/de/unirostock/sems/bives/markup/Markup.java](https://github.com/SemsProject/BiVeS-Core/tree/master/src/main/java/de/unirostock/sems/bives/markup/Markup.java)  and [JavaDoc](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/Markup.html)

Markup Document 
----------------

* represents a document that can be layouted in different formats (e.g. [HTML](TypeSetting#html) or [MarkDown](TypeSetting#mark-down))
* provides static methods to insert format independent markup:
 * [highlight](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/MarkupDocument.html#highlight(java.lang.String)): emphasizes a string (e.g. special word)
 * [rightArrow](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/MarkupDocument.html/#rightArrow()): produces a right arrow (e.g. -> or →)
 * [multiply](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/MarkupDocument.html#multiply()): produces a multiply symbol (e.g. * or ·)
 * [insert](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/MarkupDocument.html#insert(java.lang.String)): highlight something that was inserted
 * [delete](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/MarkupDocument.html#delete(java.lang.String)): highlight something that was inserted
 * [attribute](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/MarkupDocument.html#attribute(java.lang.String)): markup an attribute
* see [/src/main/java/de/unirostock/sems/bives/markup/MarkupDocument.java](https://github.com/SemsProject/BiVeS-Core/tree/master/src/main/java/de/unirostock/sems/bives/markup/MarkupDocument.java) and [JavaDoc](http://jdoc.sems.uni-rostock.de/BiVeS-Core/de/unirostock/sems/bives/markup/MarkupDocument.html)
