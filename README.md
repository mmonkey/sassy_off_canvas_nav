Sassy Off-Canvas Navigation
===========================

Off-Canvas Navigation with CSS Transitions, written in SASS and jQuery. Sassy Off-Canvas Navigation supports single-level navigation, multi-level navigation and plays nice with the rest of your code!

Version: 1.0.0

Adapted from: http://www.roblukedesign.com/trunk/trunk.html

## Introduction

Finding the perfect off-canvas navigation for responsive website developent, has prooven to be a harder task than I thought. Finding one is easy, but finding one that supports multi-level navigation, however, is not.

## Getting Started

### HTML

Using Off-Canvas Navigation, couldn't be easier, to get started add the following into the `<head>` of your html.

```html
<link rel="stylesheet" type="text/css" href="css/normalize.css">
<link rel="stylesheet" type="text/css" href="css/off_canvas_nav.css">
<link rel="stylesheet" type="text/css" href="css/style.css">
```

Link the jQuery in the `<head>` of your html.
You can add any version of jquery you would like, but as this writing, this is the latest.

```html
<script type="text/javascript" src="https://code.jquery.com/jquery-1.11.1.min.js"></script>
<script type="text/javascript" src="js/off_canvas_nav.js"></script>
```

Now inside the `<body>` tags, add the main container, off-canvas container and content-containers.

Anything you put into the `.off_canvas_container` will be displayed in the panel that slides out when the menu toggle is clicked. Also anything you put into the `.content` div will be displayed in the main area, and slide over to reveal the off-canvas navigation.

```html
<div class="container">
	
	<div class="off_canvas_animate slide off_canvas_container">

	</div>

	<div class="content_animate slide content">

	</div>

</div>
```

Add the off-canavs top menu controls. This should be in the `.off_canvas_container` div.

```html
<div class="off_canvas_animate slide off_canvas_top_menu">
	<div class="off_canvas_toggles">
		<span class="nav_prev_btn"></span>
		<span class="nav_close_btn"></span>
	</div>
</div>
```

Add the nav toggle button and your navigation to the `.content` div. I like to wrap mine in `<header>` tags

```html
<header class="content_animate slide">
	<span class="nav_toggle"></i></span>
	<nav class="dropdown">
	...
	</nav>
</header>
```

**Note:** *Any element that is not inside `.content` or any element that has a fixed position, that needs to slide away to reveal the off-canvas navigation, needs the following classes:*

```html
class="content_animate slide"
```
The same goes for off-canvas elements:
```html
class="off_canvas_animation slide"
```

### BYO Icons

All `._btn` and `._toggle` elements should be filled with your own icons and text. Out-of-the-box, these elements have very basic position-based styling.

These:
```html
<span class="nav_prev_btn"></span>
<span class="nav_close_btn"></span>
<span class="nav_toggle"></span>
```
Turn into:
```html
<span class="nav_prev_btn"><i class="icon-left"></i>Back</span>
<span class="nav_close_btn"><i class="icon-cancel"></i></span>
<span class="nav_toggle"><i class="icon-menu"></span>
```

### jQuery

Before the `</body>` tag, call the offCanvasNav() script.

```html
<script>
	offCanvasNav();
</script>
```

### Options

Some options are available when calling the offCanvasNav() script.

```html
<script>
	offCanvasNav({
		target_nav: '.dropdown',
		nav_next_btn: '<i class="icon-right"></i>'
	});
</script>
```

**Note:** *Sassy Off-Canvas Navigation needs to know what your navigation class is, because it will make a duplicate navigation and put it into the `.off_canvas_container`. The default class is `.main_nav` *

*The newly created nav is* `<nav class="off_canvas">`

## Change Log
v1.0.0 - Initial Release

by CJ O'Hara.