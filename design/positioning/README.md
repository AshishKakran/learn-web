
# Positioning 

positioning is about moving elements out of the normal document flow and display it somewhere else (as required by design). This is done by using property *position*

The initial value of the *position* property is *static*. When you change this value to anything else, the element is said to be *positioned*. An element with static positioning is thus *not positioned*

### fixed positioning

* Applying *position: fixed* to an element lets you position the element arbitrarily within the viewport.
* This is done with four companion  properties: *top, right, bottom,left*
* There is also a shorthand property available *inset* to specify the location of the elements. 
* The inset property is shortand for following related logical properties: 
	* inset-block: inset-block-start inset-block-end;
	* inset-inline: inset-inline-start inset-inline-end;
* fixed positioning is useful for creating modal dialog box
* turn off fixed positioning while printing. 

### absolute positioning

* Absolute positioning is just like fixed positioning, while *containing block* for fixed positioned element is browser viewport, the containing block for absolute positioned element is the *closest  positioned ancestor element*
* if none of element's ancestors are positioned, then the absolutely positioned element will be positioned based on something called the initial containing block. 
### Relative positioning 

* relative positioning is used to create a positioning context for an absolutely positioned element
* Relative positioning moves an element relative to its original spot in the flow. when an element is relatively positioned, the space it once occupied is preserved. Consequently overlapping can happen.
* This could be used for creating drop down menu. 


### stacking contexts and z-index

As the browser parses HTML into the DOM, it also creates another tree structure called the render tree. This represents the visual appearance and position of each element. It’s also responsible for determining the order in which the browser will paint the elements. This order is important because elements painted later appear in front
of elements painted earlier, should they happen to overlap.

This behaviour changes when you start positioning elements. The browser first paints all the non-positioned elements; then it paints the positioned ones. 

This stacking and overlapping behaviour can be manipulated with the property *z-index*

* z-index only works on positioned elements
* applying z-index to a positioned element establishes *stacking context*

A stacking context consists of a group of elements that are painted together by the browser. This implies, no element outside the stacking context can be stacked between any two elements that are inside it. If an element is stacked in front of a stacking context, no element within that stacking context can be brought in front of it and converse.

note: opacity below 1 creates stacking context, as do transform and filter properties. fixed and sticky positioning always create a stacking context even without z-index. The document root (<html>) also creates a top level stacking context for the whole page. 

All the elements within a stacking context are stacked in this order, from back to front:
 *  The root element of the stacking context
* Positioned elements with a negative z-index, along with their children
*  Nonpositioned elements
*  Positioned elements with a z-index of auto and their children
* Positioned elements with a positive z-index and their children




