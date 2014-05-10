Sassy Off-Canvas Navigation
===========================

Off-Canvas Navigation with CSS Transitions, written in SASS and jQuery. Sassy Off-Canvas Navigation supports multi-level navigation, it is easy to use.

Version: 1.0
By: CJ O'Hara

## Introduction

Finding the perfect off-canvas navigation for responsive website developent, has prooven to be a harder task than I thought. Finding one is easy, but finding one that supports multi-level navigation, however, is not.

## Getting Started

### HTML

Using Off-Canvas Navigation, couldn't be easier, to get started add the following into the `<head>` of your html.

```html
<link rel="stylesheet" type="text/css" href="css/normalize.min.css">
<link rel="stylesheet" type="text/css" href="css/off_canvas_nav.min.css">
<link rel="stylesheet" type="text/css" href="css/style.css">
```

Link the jQuery in the `<head>` of your html.
You can add any version of jquery you would like, but as this writing, this is the latest.

```html
<script type="text/javascript" src="https://code.jquery.com/jquery-1.11.1.min.js"></script>
<script type="text/javascript" src="js/off_canvas_nav.min.js"></script>
```

Now inside the `<body>` tags, add the main container, off-canvas container and content-containers.

Anything you put into the `.off_canvas_container` will be displayed in the panel that slides out when the menu toggle is clicked. Also anything you put into the `.content` div will be displayed in the main area, and slide over to reveal the off-canvas navigation.

```html
<div class="container">
	
	<div class="off_canvas_container slide">

	</div>

	<div class="top_layer content slide">

	</div>

</div>
```

Add the off-canavs top menu controls. This should be in the `.off_canvas_container` div.

```html
<div class="off_canvas_top_menu slide">
	<div class="off_canvas_toggles">
		<span class="back_btn"></span>
		<span class="close_btn">X</span>
	</div>
</div>
```

Add the nav toggle button and your navigation to the `.content` div. I like to wrap mine in `<header>` tags

```html
<header class="top_layer slide">
	<ul class="nav_toggle burger"><li></li><li></li><li></li></ul>
	<nav class="dropdown">
	...
	</nav>
</header>
```

### jQuery



Before the `</body>` tag, call the offCanvasNav() script.

```html
<script>
	offCanvasNav();
</script>
```

## Options

Some options are available when calling the offCanvasNav() script. As you can see I am telling the script that the menu toggle button is called `.nav_toggle` and the main navigation is called `nav.dropdown`

```html
<script>
	offCanvasNav({
		nav_toggle: ".nav_toggle",
		target_nav: ".dropdown"
	});
</script>
```

**Note:** *Sassy Off-Canvas Navigation needs to know what your navigation class is, because it will make a duplicate navigation and put it into the `.off_canvas_container`.*
*The newly created nav be* `<nav class="off_canvas">`