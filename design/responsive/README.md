# Responsive design

Three key principles:
* mobile first approach to design
* the @media at-rule
* Use of fluid layouts

#### Mobile first design

* A mobile layout is mostly a no-frills design. Apart from interactive menu, this design is highly focused on the content. You will want the most important content to appear first in the HTML.
* After you put the mobile styles in place, you can add medium and large breakpoints.
* screen readers use certain HTML5 elements such as *form, main, nav , aside* as landmarks. 
* use viewport meta tag

#### media queries

syntax : @media (property:value) and/or (property:value){}

* you can't access custom properties inside a media query definition*
* comparison operators are also available to use in media query definition
* media queries could be used to apply themes
* see media queries for screen and print
* too many max-width media queries could be a sign you haven't followed a mobile first approach. 

#### fluid layouts

* fluid layout refers to the use of containers that grow and shrink according to the width of the viewport
* Don't specify widths with absolute units. using percentages and ems is preferred for fluid layouts.

#### responsive Images

* serve images of different size and resolution based on media queries in stylesheet
* if you are specifying images in html markup, use srcset attribute for responsiveness
* use img { max-inline-size: 100%; } for fluid layout.
