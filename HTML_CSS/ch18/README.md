# Transitions, Transforms and Animation

* Transition requires a beginning state and an end state
	- transition-property (backgrounds, border and outlines, color, font etc)
	- transition-duration (s or ms)
	- transition-timing-function (ease|linear|ease-in|ease-out| ease-in-out|step|cubic-beizer(#,#,#,#))
	- transition-delay
	- transition: property duration timing-function delay;

* applying multiple transitions (CSS property: value1, value2;)
	- transition: <tuple1>, <tuple2>;

* Transforms

	- transform: rotate()|translate()|scale()|skew()
	- each function has its own X,Y,Z variant for more control

* applying multiple transforms
	- transform: function(value) function(value);
	- for smoothning transforms with animation or transitions

* 3D transforms

* Keyframe animations

	- @keyframes animation-name { keyframe {property:value;}, ...}

* animation properties

	- animation-name
	- animation-duration
	- animation-timing-function
	- animation-delay
	- animation-iteration-count
	- animation-direction
	- animation-fill-mode
	
