# Transform
The transform CSS property lets you rotate, scale, skew, or translate an element. It modifies the coordinate space of the CSS visual formatting model.

CSS examples: transform
- transform: translate(120px, 50%);
- transform: scale(2, 0.5);
- transform: rotate(0.5turn);
- transform: skew(30deg, 20deg);
- transform: scale(0.5) 
- translate(-100%, -100%);


![transform](https://www.htmldog.com/figures/transform.png);     



If the property has a value different than none, a stacking context will be created. In that case, the element will act as a containing block for any position: fixed; or position: absolute; elements that it contains.


The transform property allows you to visually manipulate an element by skewing, rotating, translating, or scaling:

.element {
  width: 20px;
  height: 20px;
  transform: scale(20);
}
Even with a declared height and width, this element will now be scaled to twenty times its original size:

Giving this function two values will stretch it horizontally by the first and vertically by the second. In the example below the element will now be twice the width but half the height of the original element:

.element {
  transform: scale(2, .5);
}
Or you can be more specific without using the shorthand function:

transform: scaleX(2);
transform: scaleY(.5);
But scale() is just one of many transform functions that are available:

## Values
* **scale()**: Affects the size of the element. This also applies to the font-size, padding, height, and width of an element, too. It’s also a a shorthand function for the scaleX and scaleY functions.
* **skewX() and skewY()**: Tilts an element to the left or right, like turning a rectangle into a parallelogram. skew() is a shorthand that combines skewX() and skewY by accepting both values.
* **translate()**: Moves an element sideways or up and down.
* **rotate()**: Rotates the element clockwise from its current position.
* **matrix()**: A function that is probably not intended to be written by hand, but combines all transforms into one.
* **perspective()**: Doesn’t affect the element itself, but affects the transforms of descendent elements’ 3D transforms, allowing them all to have a consistent depth perspective.


