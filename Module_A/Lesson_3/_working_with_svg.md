# Some References

[Creating Animations and Interactions with Physical Models](http://iamralpht.github.io/physics/)

[Motion Experiments](http://www.michaelvillar.com/motion)

[Interface Prototyper](http://presentplus.homerun.hr/interface-prototyper-1)

---

# PrefixFree

Make your cutting-edge CSS code compatible with mobile browser using the js library [PrefixFree](http://leaverou.github.io/prefixfree/).

---

# Working with SVG


## Export from Illustrator

- Make sure the Artboard (page size) is equal to the bounding box of all elements
- Save As SVG (regular)
- Leave default settings
- Open the svg file with brackets and remove the first 3 lines and the `width` and `height` attributes inside the main `svg` tag
- Copy the entire svg code and paste within the `article` html tag

	

### Fix wrong calculated height in older webkit

	

There also a Javascript way to do the same (to be tested):

[A vanilla JavaScript fix (of sorts) for responsive SVGs in Safari and some other WebKit browsers.](https://gist.github.com/benfrain/5880387#file-jsfixforresponsivesvgsinsafari-js)




