# Mobile WebApp basic Layout


## HTML

The basic HTML document

	<html>
	
		<head>
		</head>
		
		<body>
		</body>
		
	</html>
	
	
The required meta tag for Mobile browsers

	<meta name="viewport" content='width=device-width,initial-scale=1,maximum-scale=1,user-scalable=0' />
	<meta name="apple-mobile-web-app-capable" content="yes" />
	<meta name="apple-mobile-web-app-status-bar-style" content="black">
	<meta name="mobile-web-app-capable" content="yes" />
	
	

## CSS

### Resets and Defaults

	* {
		user-select: none;
		box-sizing: border-box;
	}
	
	html, body {
		padding: 0;
		margin: 0;
		width: 100%;
		height: 100%;
		overflow: hidden;
		display:flex;
		flex-direction:column;
	}
	
## Helper selectors

Add scroll behaviour to container with momentum

	.myContainer{
		overflow-x:auto;
  		-webkit-overflow-scrolling: touch;
	}


## Flex

Flex is a powerful CSS module that let to layout everything in efficient way (means without hacks). It is not ready for production websites but it is perfect for prototyping purposes.

Here some nice articles about it:

[A Complete Guide to Flexbox](http://css-tricks.com/snippets/css/a-guide-to-flexbox/)

[Solved by Flexbox](http://philipwalton.github.io/solved-by-flexbox/)

Example: to center horizontally and vertically children in container:

	.myContainer{
		display: flex;
		justify-content:center;
		align-items:center;
	}


## Best Practices

Use an external CSS file if you are in local development

	<head>
		<link rel="stylesheet" type="text/css" href="style.css" />
	</head>
	
	
	
# SVG

### Fix wrong calculated height in older webkit

Some older webkit calculate the height of svg with fluid width.
This is the fix if you want to show fluid svg on older webkit (like iOS7 or the build-in Android browser)

Add this css rules

	object {
		width: 100%;
		display: block;
		height: auto;
		position: relative;
		/* This is the ratio percentage (100% means square, 50% rect with height = width/2 and so on)
		padding-top: 100%;
	}
	
	svg {
		width: 100%;
		height: 100%;
		position: absolute;
		top: 0;
		left: 0;
	}
	
And the svg must be contained in object tag like:

	<object>
		<svg>...</svg>
	</object>
	

There also a Javascript way to do the same:

[A vanilla JavaScript fix (of sorts) for responsive SVGs in Safari and some other WebKit browsers.](https://gist.github.com/benfrain/5880387#file-jsfixforresponsivesvgsinsafari-js)
