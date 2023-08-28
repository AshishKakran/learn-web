# Colors and Backgrounds

**specifying color**
- by name
- value of rgb (numeric or hexadecimal)
- color schemes supported by CSS is rgb/rgba and hsl (not hsb)

**foreground color**
- color

**background color**
- background color (value|transparent(default), not inherited)
- clip background by background-clip
- specify opactiy with opacity property


**pseudo-class selectors** (:)
1. linke pseudo-class
 - :link
 - :visited
 - :active
 - careful for touch devices

2. other pseudo-classes selectors include (structural, input,location, linguistic, logical and 40 more)


**pseudo-element selectors** (::)
- ::first-line
- ::first-letter
- generated content with ::before and ::after


**attribute selectors** 
- element[attribute]
- element[attribute="exact value"]
- element[attribute~="value"] (contains logic)
- ~ for contain, ^ for first part , $ for last part, * for any part , | for variation

**Background images**
 - background-image: url (can be added to any element, no inherit)
 - background-repeat: repeat | no-repeat | repeat -x/y | space | round
 - background-position: length | percentage | left |center | right|top|bottom
 - background-attachment : scroll | fixed | local
 - background-size: length | percentage| auto | cover | contain
 - background (shorthand property) (handy for multiple backgrounds)

**gradients** ( can be applied to background,border-images, list-style-images)
- linear gradient (position, colors)
- radial gradient (position, color,shape, size)
- repeating-linear-gradient

**external style sheets**
- link
- import
- modular design 