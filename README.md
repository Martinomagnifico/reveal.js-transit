# reveal.js-transit
A plugin for [Reveal.js](https://revealjs.com) that checks if slides and fragments are done transitioning.


Sometimes you want effects, images, graphs etc to kick in only *after* a slide in Reveal.js has ended the slide transition. Reveal.js has no "slidechangecomplete" event (or other cool name), so this plugin does just that. 


It is likely that a future version of Reveal.js wil make this plugin obsolete :-)


Here's a [demo](https://martinomagnifico.github.io/reveal.js-appearance/demo.html) of a project that also uses this transit.js plugin.


Transit.js does multiple things:
* Emits an event "slidechangecomplete" after a slide has completed its transition. The current and past slides are still available as event.currentSlide and event.previousSlide
* Emits an event "fragmentshowncomplete" after a fragment has completed its "shown" transition. The fragment is available as event.fragment.
* Emits an event "fragmenthiddencomplete" after a fragment has completed its "hidden" transition. The fragment is available as event.fragment.
* Adds a class "done" on slides and fragments that have completed 


## Installation

Copy the transit folder to the plugins folder of the reveal.js folder, like this: `plugin/transit`. Now add it to the dependencies of Reveal.js:


```javascript
Reveal.initialize({
	// ...
	dependencies: [
		// ... 
		{ src: 'plugin/transit/transit.js' },
		// ... 
	]
});
```

## Like it?
This is my third Github repo... let me know if you like it.


## License
MIT licensed

Copyright (C) 2019 Martijn De Jongh
