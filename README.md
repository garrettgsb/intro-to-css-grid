# Grid vs. Flexbox

First: It's not a competition. Grid and Flexbox play very well together, and modern layouts are likely to use both in concert.

**2 dimensions vs. 1 dimension**

Designing with Flexbox is essentially designing in one dimension at a time: Two-dimensional layouts can be made by nesting flexboxes. This is very powerful and expressive, but sometimes we end up with markup that exists only for layout-- Something that we prefer to avoid.

Also: In two-dimensional layouts using Flexbox, we can only tell items to arrange along one dimension. If we want both horizontal _and_ vertical alignment, we are stuck.

Grid solves both of these problems by allowing grid items to orient themselves along two dimensions, instead of just one.

**Grid items (sometimes) know that they're grid items**

Flex items can live their entire lives without knowing that they are flex items, and indeed, that is how it usually goes. Occasionally, one may express an opinion about the proportion by which it should `flex-grow` or `flex-shrink`, and particularly ambulant flex items may decide to change their `order`.

But grid items are cut from a different cloth. They are often individually responsible for making all sorts of decisions about which part of their container they will occupy.

That said, a grid can be created in such a way that items can just be inserted into it naively, and the grid will arrange them nicely, with the same cleverness and care of a flexbox.

**Grids are more hands-on**

With Flexbox, we really only need to make one decisions:

* Is it a flexbox? (`display: flex`... This one is easy)

There is some secondary configuration that is fairly common, in case the reasonable defaults don't solve our problem:

* Column or row? (`flex-direction`)
* How are things positioned on the main axis? (`justify-content`)
* How are things positioned on the cross axis?

With Flexbox, the behavior governing the flex items is defined, and then the items are arranged implicitly.

With a grid, a more elaborate `grid-template` is defined, and the items are arranged within it either explicitly or implicitly.

Sometimes, `display: flex` is all you need. `display: grid` by itself will not do much.

# Key Terminology

* Grid container - Any element with `display: grid`
* Grid item - Any direct descendent of a grid container
* Grid line - Any of the lines drawn by the grid
* Grid cell - The smallest division defined by the grid lines
* Grid track - A row (horizontal track) or column (vertical track)
* Grid area - An area that spans one or more cells
* Grid gap - The space between cells

# Properties To Know

## Core Properties

**On a grid container:**

* `display: grid`
* `grid-template-rows`
* `grid-template-columns`
* `grid-template-area`

**On a grid item:**

* `grid-column`
* `grid-row`
* `grid-area`

## Pretty Useful Properties

`grid-gap`

**`-content` moves the grid around in its container**

* `justify-content`
* `align-content`


**`-items` moves each item around in its grid area**

* `justify-items`
* `align-items`

# Key Tools

`minmax()`
`fr` units

# References

[Incredibly Easy Layouts with CSS Grid](https://www.youtube.com/watch?v=tFKrK4eAiUQ)

[CSS Grid: Moving From CSS Frameworks To CSS Grid](https://www.youtube.com/watch?v=paMmgo4MhQ8)

[Why CSS Grid Is A Game Changer For Web Design](https://www.youtube.com/watch?v=dIrz8WNxNxE)

[CSS Grid Changes EVERYTHING](https://www.youtube.com/watch?v=7kVeCqQCxlk)
