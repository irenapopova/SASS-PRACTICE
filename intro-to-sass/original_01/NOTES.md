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



#### In HTML there are inline and block elements , anchor tags are example for inline elements, If I have two anchor tags after each other they are rendered in the same line. They do not take the full entire width as block level elements do. Both use the box model though for the inline element, we cannot really set a margin top and bottom, because inline elements are not positioned in the flow like the block  level elements. They do not take a new line necessarily, hence margin top and bottom is difficult because they might be inline with another element. 
The behavior can be changed with the display property. 

##### the default value for an anchor tag is inline, but the value can be changed to block, 
##### the idea behind display:none; is that it is especially useful if it is used in conjunction with JavaScript, for example to show it after a button was clicked. This allows to create models which only show up on certain action, 

##### the class that I assign to my list <li></li> items 



#### display: none vs visibility: hidden
We had a look at display: none;  - this value removes the element to which you apply it from the document flow. This means that the element is not visible and it also doesn't "block its position". Other elements can (and will) take its place instead.

There is an alternative to that though.

If only want to hide an element but you want to keep its place (i.e. other elements don't fill the empty spot), you can use visibility: hidden; 

Here's a visual example:
```css
.box-1 {
    display: none;
}
 
.box-2 {
    display: inline-block;
}
```
Will render:

x  

where x  has the class box-2 . The first element just isn't displayed. It's still part of the DOM though, you can still access it via JavaScript for example.

Here's an example for visibility: hidden :
```css
.box-1 {
    visibility: hidden;
}
 
.box-2 {
    display: inline-block;
}
```
Will render:

_x 

where _  simply is an empty spot and x  has the class box-2 .

The element is only invisible, it's not removed from the document flow and of course also not from the DOM.

#### Block-level elements are rendered as a block and hence take up all the available horizontal space. You can set margin-top and margin-bottom and two block-level elements will render in two different lines.

Some examples are: <div> , <section> , <article> , <nav>  but also <h1> , <h2>  etc and <p> .

Inline elements on the other hand only take up the space they require to fit their content in. Hence two inline-elements will fit into the same line (as long as the combined content doesn't take up the entire space in which case a line break would be added).

They also use the box-model you learned about but margin-top  and margin-bottom  have no effect on the element. padding-top  and padding-bottom  also have a different effect. They don't push the adjacent content away but they will do so with the element border. You can read more about that behavior in the following article: https://hacks.mozilla.org/2015/03/understanding-inline-box-model/

Additionally, setting a width  or height  on an inline element also has no effect. The width and height is auto to take as much space as required by the content.

Logically, this makes sense since you don't want your inline elements to destroy your multi-line text-layout. If you want to do so or need both block-level and inline behavior, you can set display: inline-block  to merge behaviors.

Some example elements are: <a> , <span> , <img> 

#### Pseudo Classes and Pseudo Elements

What is the difference?