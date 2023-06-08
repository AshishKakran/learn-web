# CSS Flexbox layout and Grid

**setting up a flexbox container**
 - display (flex)

**controlling "flow" within the container**
 - flex-direction (row|column)
 - flex-wrap (wrap|no-wrap|wrap-reverse)
 - flex-flow (flex-direction flex-wrap)
 
**controlling the alignment of flex items in the container**
 - jusitfy-content (flex-start|flex-end|center|space-between|space-around) ( controls main axis alignment)
 - align-items (controls cross axis alignment)
 - align-self (individual flex item alignment)
 - align-content (aligning multiple lines)
 - aligning items with margin (e.g navigation items and logo) (margin-right|margin-top)

 **Determining how items "flex" in the container**
 - flex (none|flex-grow flex-shrink flex-basis);
 - flex-grow (0|1|integer)
 - flex-shrink(0|1|integer)
 - flex-basis (length|percentage|content|auto)
 - shortcuts:
    -- flex:initial (0 1 auto)
    -- flex:auto (1 1 auto)
    -- flex:none
    -- flex:integer (integer 1 auto)
 - absolute vs relative flex
 - container vs flex item properties

 **Changing the order of flex items**
 - order (integer) (smallest to largest)
 - spacing caveats

 **setting up grid areas**
 - diplay: grid;
 - grid-template-rows: [row-names] grid-units(px, em, fr);
 - grid-template-columns: [column-names] units
 - grid-template-areas: "row-wise names";
 - repeat, minmax(min, max), min-content, max-content,auto

 - grid: [start line name] "area names" <track size> [end line name]

**placing items in grid**


