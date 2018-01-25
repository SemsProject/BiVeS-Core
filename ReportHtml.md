Report encoded in HTML 
=======================

For convenience, BiVeS also produces an HTML report which can simply be included into existing web interfaces. For example, you can just dump it into a `div` container of your website. To highlight different parts in the report BiVeS add some CSS classes to the element and you just need to define additional CSS rules, such as:

```css
.bives-insert
{
  /* inserts - color them green for example */
}
.bives-delete
{
  /* deletes - color them red for example */
}
.bives-update
{
  /* updates - color them orange for example */
}
.bives-move
{
  /* updates - color them blue for example */
}
.bives-attr
{
  /* attributes - make them bold and italic for example */
}
.bives-suppl
{
  /* supplemental entities that can be hidden */
}
bives-table-left
{
  /* first coloumns in tables (identifying the entities) - bold for example */
}
bives-table-right
{
  /* second coloumn of tables (displaying the definition of entities) */
}
bives-math
{
  /* math will we enclosed in .bives-math, you might want to hide it? */
}
bives-math-original
{
  /* the original math terms */
}
bives-math-modified
{
  /* the modified math terms */
}
```

Here, `.bives-suppl` is used for entities that do not describe differences. They are just included to provide a better overview over the model. You might want to set them to `display: none;` to decrease the bloat, and instead add a button which toggles their visibility.