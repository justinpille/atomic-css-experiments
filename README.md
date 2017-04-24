# atomic-css-experiments
A readme-only project for organizing my aspirations in atomic CSS.

Atomic CSS means writing single-purpose classes and composing them at the point of use. You can read about the benefits of this approach at the links below:

- [CSS and Scalability](http://mrmrs.io/writing/2016/03/24/scalable-css/)
- [Functional Programming, CSS, and your sanity](http://www.jon.gold/2015/07/functional-css/)

I'm creating a series of opinionated design systems, with predifiend classes geared toward the atomic philosophy. Each system can be paired with a design kit, including things like paper templates. The idea is that designers and developers can agree upon a system, then work somewhat independently using their own tools.

Modules could be combined within a project, or even used to extend a framework like [basscss](http://basscss.com/)
. Mainly these are experiments and I don't expect them all to be practical. I hope to learn a lot.


## Base Ten

An algrabraic positioning system where the smallest unit is 10 pixels. Class names are short abbreviations postfixed with a multiplier. `p1` is `padding: 10px`, and `m7` is `margin 70px`.


## Geometric Space

A positioning system where distances increase geometrically. The 1 index is 1px, and each subsequent index is obtained by doubling. 

1. 1
2. 2
3. 4
4. 8
5. 16
6. 32
7. 64
8. 128
9. 256
10. 512
11. 1024
12. 2048

So for example, `p6` maps to `padding: 8px`.


## Imperial Columns

The familiar 12 column grid. Widely used because 12 is divisible by 2, 3, 4, and 6 (not to mention 1 and 12). Use `col-2` to denote that an element should take up two of the twelve columns (i.e. one-sixth of the width of the parent container). Widths are difined in percentages, so they will squish and expand as the container size changes.



## Divider

A grid system with units that divide instead of multiply. `col-1` is 100% width, `col-2` is 50%, and `col-3` is 33.33%. It goes up to `col-12`, which is 8.33%.


## Quad 1

From Wikipedia, 
> The axes of a two-dimensional Cartesian system divide the plane into four infinite regions, called quadrants, each bounded by two half-axes.

The quadrants are numbered, and the one on the top-right is number 1. If you take the browser's viewport to encompass that quadrant you would have a system where the bottom-left corner of the screen is the origin, and X and Y increase when going right and up.

Computer graphics systems, including CSS, tend to follow the paradigm of western writing systems: Start from the upper-left and go right. When you run out of space go down a line and start again from the left. To make CSS work like quadrant one we'll change the way that it lays out text.


## Aspect




## Golden Columns

Columns of unequal width, based on the fibonacci sequence.


## Position by Numbers

Regionas are defined and numbered. Elements can be placed in any region by using the correct number as a class name.



## Offset

Offset refers to the CSS properties `top`, `right`, `bottom`, and `left`. The classes in this module are named as such, followed by multiplier (e.g. `top-1`). Offsets are ignored in statically positioned elements, and this module assumes that anything with an offset should be absolutely positioned.



## Margin

Utilizes positive and negative margins. Odd indexes represent the negative equivalent of the previous even index.



## Animation

Units of `.25s` for `transition-duration`. The class `anim-3` applies the following CSS:
```css
.anim-3 {
  transition-property: all;
  transition-duration: .25s;
}
```


## Colors

Each color class is both a background color and a complimentary text color.


## Hedges

Decoration for the outside edges of an elements property line. Outlines, borders, and box-shadows.



## Rule of Thirds

The Rule of Thirds is a tool for photographic composition. It's usually depicted by a picture with 4 lines drawn over it: Two vertical and two horizontal. It appears as if you're creating 9 regions, but the point is actually to use the intersections as focal points. With this module you position each object relative to one of the four focal points.
