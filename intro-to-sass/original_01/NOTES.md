#### inheritance 

Inheritance means that an element also inherits some styles of the parent element. 
Inheritance is an important concept for passing styles down whithout explicitly selecting an element.

#### Understanding Combinators 

### Adjacent Sibling 
is adding by adding a plus + between the selectors I want to apply, I can add more 


div + p {
    color:blue;
}




#### Chid
#### General Sibling
#### Descendant

##### Selectors 

div
.blog-post
#main-title
[disabled]
*

##### Properties 
background-color
width
color
margin
display

#### Values


#### Value Types 

Values are tightly coupled to specific property

#### pre-defined options 

display: block;

overflow: auto;

#### colors

background: red;
color: #f2dff;
color: #fff;

#### Length, sizes, numbers

height: 100px;
width: 20%;
order: 1;

#### Functions

background: url(...);

transform: scale(...);

Every element in HTML is interpreted as a box by CSS, and 

margin is space around the element 

#### Margin Collapsing 
If I have two elements next to each other, then margin between them are actually collapsed to one margin. And the bigger margin wins.

When working with margins, you can get unexpected results. 

Why are two adjacent elements sharing one margin even though each element has its own one?
Why does a parent element (e.g. <section>  as in the videos) suddenly take on the margin of the child element (e.g. <h1> )?
It's always related to margin collapsing. You can dive deeply into it with the help of the following awesome article: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model/Mastering_margin_collapsing

There, three base cases are described:

Adjacent siblings which both have margins
A parent which holds one or more child elements where the first and/ or last (or the only) child has margins
An element without content, padding, border and height
Let's explore these cases:

1. Adjacent Siblings

In this case, the first element might have a margin of 10px  (on all sides let's say) and the second one has 5px  (or 20px  - the values don't matter).

CSS will collapse the margins and only add the bigger one between the elements. So if we got margins of 10px  and 5px , a 10px  margin would be added between the elements?

2. A parent with children that have a margin

To be precise, the first and/ or last or the only child has to have margins (top and/ or bottom). In that case, the parent elements margin will collapse with the child element(s)' margins. Again, the bigger margin wins and will be applied to the parent element.

If the parent element has padding, inline content (other than the child elements) or a border, this behavior should not occur, the child margin will instead be added to the content of the wrapping parent element.

3. An empty element with margins

This case probably doesn't occur that often but if you got an element with no content, no padding, no border and no height, then the top and bottom margin will be merged into one single margin. the bigger one wins.


#### shorthands properties 

Combine values of multiple properties in a single property (the shorthand property)

### Block level elements are like inline elements, always take the full available width by default. 

#### Note
If I want to style the height of an element relative to the height of the page , I need to create such a chain where to pass the page height down . 
#### Understanding Box Sizing 
All elements by default have a certain way of calculating width and height which is called content box.