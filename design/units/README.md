
### Relative units

*Length* is the formal name for a CSS value that denotes a distance measurement. Its a number followed by a unit, such as 5px. Percentages are similar to length, but not technically the same thing.

* CSS provides a wide array of options to choose from when it comes to specifying length values, such as px (absolute units) and em, rem (relative units). 
*  1 in. = 6 pc (1 pc  =12 points) = 72 pt = 96px (this can vary)
* *Responsive design* refers to styles that "respond" differently, based on the size of the browser window.

<h5> Ems and Rems </h5>

 * 1em on a property means 1 x size of font-size of the element it is applied to. This font size could be inherited. 
 * Values declared using relative units are evaluated by the browser to an absolute value  called *computed value*   
 * If you know the pixel-based font size and you want to specify it in ems. then divide desired pixel size by the parent (inherited) pixel size
 * for most browsers, the default font size is 16 px. Technically its the keyword value *medium* that calculates to 16 px.
 * Ems get tricky when you use them both for font size and any other properties on the same element because of inheritance.
 * Ems can produce unexpected results when you use them to specify the font sizes of multiple nested elements - classic shrinking font problem in nested lists. 
 
** Use rems for font-size, pixels for borders and either ems or rems for most other properties. **

<h5> Viewport-relative units </h5>

*vh* - 1% of the viewport height
*vw* - 1% of the viewport width
*vmin* - 1% of the smaller dimension
*vmax*  - 1% of the larger dimension

similar we have svh, svw, lvh, lvw and dvh, dvw analogues units.

*  viewport units don't take scrollbars into account
* CSS specification doesn't dictate whether an onscreen keyboard should shrink the small viewport size
* The original viewport units generally behave like large viewport units in most browsers (not guaranteed)
* Use dynamic viewport units sparingly as it can cause layout thrashing if element heights change dynamically.
* See code for example of using viewport units for font-size. Always make sure to include ems or rems in calculation for accessibility. 
* see calc(), clamp() and min() and max() functions

<h5> unitless numbers and line-height </h5>

Some properties allow for unitless values e.g *line-height, z-index and font-weight*.

A unitless 0 can be used only for length values and percentages such as in paddings, borders and widths. It can't be used for angular values or time-based values.

Unusually, line-height property accepts both units and unitless values. Prefer using unitless numbers as they are inherited for each children.

* When an element has a value defined using a length(px,em, rem), its computed value is inherited by child elements
* When we use unitless number, that declared value is inherited, meaning its computed value is recalculated for each inheriting child elements. 

### CSS variables (custom properties)

* variables must be declared inside a declaration block
* Declaration of custom properties cascade and inherit. they  can be overridden for child elements

Declaration syntax: 

`:root {
	--main-font: Helvetica, Arial, sans-serif;
}`

Using its value
`p {
	font-family: var(--main-font, sans-serif) /*see fallback */
	} `

If a var() function evaluates to an invalid value, the property will be set to its initial value. 



