# Designing with flexbox

### flexbox principles

A flexbox container assets control over the layout of the elements within. You set `display: flex` on an element and its children elements are converted into flex items which align left to right by default. flex is one-dimensional layout. 
It has the main axis (from main-start to main-end) and cross axis (from cross-start to cross-end).

subtle points:
* if flex items are inline type, turn them to block type. otherwise height they contribute to their parent would be derived from their *line-height*, not their padding and content
* flexbox allows you to use *margin:auto* to fill all available space between flex items.
* a flex container will be 100% the available width, but the height is still determined naturally by its contents. This behaviour doesn't change when you rotate the  main axis
* In a vertical flexbox, `flex-grow` and `flex-shrink` applied to the items will have no effect unless something else forces the height of the flex container to a specific size.
* be careful with the use of order. Assistive tech will follow source order in most cases.

properties:

	flexflow: flex-direction flex-wrap
	flex: flex-grow flex-shrink flex-basis
	gap (for specifying gap between flex items)
	justify-content (positioning along main axis)
	align-items (alignment along cross axis)
	align-content (multiline alignment)
	align-self (applies to flex items)
	order (-ve to +ve)

In general, you’ll begin a flexbox with the methods we’ve already covered:
* Identify a container and its items and use display: flex on the container
* If necessary, set a gap and/or flex-direction on the container
* Declare flex values for the flex items where necessary to control their size

Once you’ve put elements roughly where they belong, you can add other flexbox
properties where necessary.

