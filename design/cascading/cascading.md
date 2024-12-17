Cascading in CSS determines how conflicts are resolved. When facing a styling problem, First, figure out what declaration will get it looking right, and second, think through the possible ways to structure the selectors and choose the one that best fits your needs.

The browser follows these cascading steps to resolve every property for every element on the page. A cascaded value is a value for a particular property applied to an element as a result of the cascade. 

### Syntax 
`
	property : value;

	selector {
		property: value;  /* These are called declarations */
	} /* declaration block */
`

selector + declaration => ruleset (rule)

### Cascading Rules

If you add a declaration to your CSS and it seems to have no effect, often it's because a more specific rule is overriding it. 

1. Stylesheet origin ( author << user >>  user-agent styles)
		Declarations marked `!important` are treated as a higher priority origin, so they will always override normal styles from any region. 
		 *Important u-a >> Important user >> Important author >> author >> user >> u-a*

2. Inline styles overrides origin based rules. 
		To override inline declarations, add an `!important` to the declaration, shifting it into a higher-priority origin.  
		
3.  Selector specificity 
		 Different types of selectors also have different specificities. 
		 ( #inline, #id, #class, #selectors)
		 (0,1,0,0) > (0,3,0,0)
		 (0,2,0,0) > (0,1,3,3)
		 (0,0,1,0) > (0,0,0,5)

4. Source order
		 If all the other criteria are the same, then the declaration that appears later i the stylesheet - or appears in a stylesheet included later on that page - takes precdence.
		 Selectors for styling links should in a certain order. -> Link, visited, hover, active.

![[Pasted image 20241217111813.png]]


### Inheritance 

If an element has no cascaded value for a given property, it may inherit one from an ancestor element. Not all properties are inherited though.  Inherited properties are mostly related to text : `color, font, font-family, font-size, font-weight, font-variant, font-style, line-height, letter-spacing, text-align, text-indent, text-transform, white-space and word-spacing`.

### Special values

1. inherit keyword (`property: inherit;`)
2. initial keyword (`property: initial;`)
		Every CSS property has an initial or default value. Assigning value `initial` to that property effectively resets to its default value. Its like hard reset
3. Unset keyword (`property: unset;`)
		When applied to an inherited property, it sets the value to `inherit`, and when applied to a non-inherited property, it sets the value to `initial`.

4. Revert Keyword (`property: revert;`)
		The `initial` and `unset` keywords essentially override all styles, from both author and user-agent stylesheets. To override previously set author styles but leave the user-agent styles intact use `revert`.

These keywords are normal cascaded values. That means it is still possible to override them with other values when another selector with higher specificity targets the same element.

### shorthand properties

Some shorthand properties like `font`, `background`, `border` has subtleties.
-> Omitting certain values still sets the omitted values to their initial value.
-> In some shorthand properties like `margin` and `padding`, order is important. If a property specifies two measurements from a corner(like `background-position`, `box-shadow` and `text-shadow`) think "Cartesian grid". If a property specifies measurements for each side all the way around an element, think "Clock" (top, right, bottom, left)

	E.g `margin: margin-top margin-right margin-bottom margin-left;`


### progressive enhancement

You can add the CSS needed to provide an acceptable (but less full-featured) experience to older browsers, and then you can layer on CSS using newer features, knowing those particular features will only work in the newest browsers. This approach is called progressive enhancement .

**when a ruleset has multiple selectors, the browser will ignore the entire ruleset if any of the selectors are unsupported or invalid. Best option is to decouple them and write separate rules**

We can use feature query @supports to check whether a particular rule is available in a browser or not.

	E.g `@supports (display: grid) {....}`
		`@supports not (<declaration>)`
		`@supports (<declaration>) and/or (<declaration>)`
		`@supports selector(:user-invalid)`

First provide a fallback option for old browser, followed by a feature query that give a full featured new option. This is resilient CSS. 

Important links

<a href="https://caniuse.com/"> CanIUse.com </a>



