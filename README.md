# CSS-FLEXBOX-DESCRIPTION

Sizing Elements and Handling Overflow | Cheat Sheet
1. Sizing Elements
1.1 Intrinsic Size

Some elements have a natural size set by default, we call it Intrinsic Size.
HTML
CSS
JAVASCRIPT
Inspect
 

In the example above, the default sizes are applied to the image and paragraph elements.
1.2 Extrinsic Size

If we set a Specific Size to an element, we call an Extrinsic Size.
HTML
CSS
JAVASCRIPT
Inspect
 

In the example above, a specific size was given to the image and paragraph elements.

2. Handling Overflow
2.1 CSS Overflow Property

Content overflow can be handled using the CSS overflow
 property.

The overflow property has the following values:

    visible
    (default) - CSS tries to avoid data loss. Hence, the overflow: visible;
    is the default value for it.
    hidden
    - The overflow is clipped, and the rest of the content will be invisible.
    scroll
    - The overflow is clipped, and a scrollbar is added to see the rest of the content.
    auto
    - It is similar to scroll
    , but it adds scrollbars only when necessary.

Try out CSS overflow
 property with different values in the below Code Playground.
HTML
CSS
JAVASCRIPT
Inspect
 
2.2 overflow-x & overflow-y

There are two other CSS properties similar to overflow
, which is used for handling in any one particular direction.

    overflow-x
    - To handle overflow in the horizontal direction.
    overflow-y
    - To handle overflow in the vertical direction.

HTML
CSS
JAVASCRIPT
Inspect
 
 

3. Min & Max Sizes
3.1 Min size

The min-height
 & min-width
 CSS properties can be used to define the minimum sizes of an element.
CSS
3.2 Max size

The max-height
 & max-width
 CSS properties can be used to restrict the sizes of an element.
CSS
3.3 Min & Max Sizes with Overflow

If the content needs a larger than maximum height, the overflowing of content can be observed.
HTML
CSS
JAVASCRIPT
Inspect
 

4. A Note on Meta Element
HTML

The meta
 element is used to provide additional important information about HTML document.

    Name - specifies the type of meta element it is, what type of information it contains. viewport
    gives instructions to browsers on how to control the page's dimensions and scaling.
    Content - specifies the actual meta content.

Note
In mobile devices, you may experience this issue, so it is a good practice to include viewport meta
element in the HTML.
5. Summer Collection Section Example - Final Code















CSS BOX SIZING 




Box Sizing | Cheat Sheet
1. Box Sizing

Every HTML element on a web page is a rectangular box.

By default in the CSS box model, the width
 and height
 you set to an element are applied only to the element's content.
HTML
CSS
JAVASCRIPT
Inspect
2. The box-sizing Property

The box-sizing
 CSS property sets how the total width
 and height
 of an element are calculated.

Box-sizing Property has the following values:

    content-box
    (default)
    border-box

2.1 Content Box

The width
 and height
 properties include the content, but they do not include the padding
, border
, or margin
.
HTML
CSS
JAVASCRIPT
Inspect
2.2 Border Box

The width
 and height
 properties include the content, padding
, and border
, but they do not include the margin
.
HTML
CSS
JAVASCRIPT
Inspect
Note

    Bootstrap uses box-sizing: border-box;
    for all the HTML Elements.
    It's better to use box-sizing: border-box;
    while developing layouts.

3. Universal Selector (*)

 Selects all the HTML elements within the document.

Syntax :
* {
  property1: value1;
  property2: value2;
}
HTML
CSS
JAVASCRIPT
Inspect
Note
Styles applied using a universal selector will have the lowest specificity.



---------------------------------------------------------------------------------------------------------------------------
Introduction to CSS Flexbox | Cheat Sheet
1. Layout

A Layout is a pattern to structure the information and arrange the elements on the website.
1.1 Methods to Design a Layout

Mainly, there are two methods that help design the webpage layout.

    Flexbox (stable)
    CSS Grid (Advanced & Fast growing but not stable)

1.1.1 Flexbox

Flexbox is a layout method that helps to arrange the HTML elements in rows (horizontally) or columns (vertically).
2. Flexbox Layout with CSS Properties

To achieve flexbox layout CSS provides many properties, these are a few among them.

    display
    flex-direction
    justify-content
    align-items
    flex-wrap
    flex-flow
    align-content
    align-self
    flex-grow
    flex-basis
    flex-shrink
    order and many more...

2.1 Display

To achieve different Layouts, we can use CSS property display
.

Display property can have the following values:

    flex
    inline-flex
    grid
    none
    and many more...

Providing display property with the value flex
 converts the element into a Flex Container. All HTML elements that are direct children of Flex Container are called Flex Items.
HTML
CSS
JAVASCRIPT
Inspect

In the example above, irrespective of inline or block elements, the Flex Container handles the display of Flex Items.
2.2 Flex Direction

The Flex Direction specifies the direction of the flex items in the Flexbox Container.

When working with Flexbox layout, we need to think in terms of two axes.

    Main Axis- It is specified by the flex-direction
    property.
    Cross Axis- It runs perpendicular to the main axis.

Flex Direction property can have the following values:

    row
    - Direction of the flex items is horizontal.
    column
    - Direction of the flex items is vertical.

HTML
CSS
JAVASCRIPT
Inspect

In the example above, try out flex-direction
 property with different values.
2.3 Justify Content

The justify-content
 property specifies the alignment of flex items along the main axis.

Justify Content property can have the following values:

    flex-start
    (default) - All the elements will arrange to the start of the container.
    center
    - All the elements will arrange to the center of the container.
    flex-end
    - All the elements will arange to the end of the container.
    space-between
    - Left over space will be arranged in between the flex items.
    space-around
    - Every flex item will get space around them.

HTML
CSS
JAVASCRIPT
Inspect

In the example above, try out justify-content
andflex-direction
 properties with different values.
2.4 Align Items

The align-items
 property specifies the alignment of flex items along the cross axis.

Align Items property can have the following values:

    stretch
    (default)- Will stretch its available height.
    flex-start
    - Will be at the starting of the flex container.
    center
    - Will be at the center of the avilable height.
    flex-end
    - Will be at the ending point of the available height.

HTML
CSS
JAVASCRIPT
Inspect

In the example above, try out align-items
andflex-direction
 properties with different values.

3. Music Section Example - Final code

----------------------------------------------------------------------------------------------------------------------------------------


CSS Flexbox > Introduction to CSS Flexbox | Part 2 | Cheat Sheet
Win
10 Points
Introduction to CSS Flexbox | Part 2 | Cheat Sheet
1. Flex Wrap

The flex-wrap
 property arranges the flex items in multiple lines.

Flex Wrap property can have the following values:

    nowrap
    (default)
    wrap
    wrap-reverse
    and many more...

HTML
CSS
JAVASCRIPT
Inspect
 

In the example above, try out the flex-wrap
 property with different values by changing the flex-direction
.

2. Frontend Developer Section Example
Initial Code
HTML
CSS
JAVASCRIPT
Inspect
 
 
Final Code
HTML
CSS
JAVASCRIPT
Inspect
 
 

Flex Item can also be a Flex Container.

In the example above, class name bg-container acts as a flex container, and cards-container acts as a flex item to bg-container.

Similarly, the class names with the card act as flex items to the cards-container. Here cards-container behaves as a flex container for all the class names with the card.

3. Shoes Shopping Section Example
Initial Code -----------------------------------------------------------------------------------------------------------------------------------------------------




Introduction to CSS Flexbox | Part 3 | Cheat Sheet
1. Align Self

The align-self
 property specifies the alignment of Individual Flex Items along the cross axis.

Align Self property can have the following values:

    flex-start
    center
    flex-end
    stretch
    auto
    (default) and more...

If the value of align-self
 is auto
, then the align-items
 value of its Flex Container gets inherited.
HTML
CSS
JAVASCRIPT
Inspect

In the example above, try out the align-self
 property with different values by changing the flex-direction
.

2. Order

The order
 property specifies the order of Flex Items in the Flex Container.

Order property has the following values:

    0 (default)
    +ve values
    -ve values

HTML
CSS
JAVASCRIPT
Inspect

In the example above, try out order
 property with different values.
Note
If two or more HTML elements have the same order, then they will be arranged based on their source code.

3. Chat Screen Example
Initial Code


-----------------------------------------------------------------------------------------------------------------------------------




