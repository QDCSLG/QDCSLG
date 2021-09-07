
# : vs ::
Every borwser that supports the double colon css3 syntax also supports just the : syntax. But IE 8 only supports the single colon. So it is recommended to  just use single-colon for best browser support. If no need to support IE 8, then use the double colon

# pseudo-class vs pseudo-element

- pseudo-element is a keyword added to a selector that lets you style a specific part of the selected element for example `::ifrst-line` can be used ot change the font of the first line of a graph
- pseudo-class can be used to style an element based on it state. It is a keyword added to a selector that specifies a special state of the selected element. For example `:hover` can be used to change a button color when user's point hovers over it.

# ::before and ::after

these two are the pseudo-eleents in CSS allows you to insert content onto a page without it needing to be in the HTML. While the end result is not actually on the DOM, it appears on the page as if it is

The only reasons to use one over the other are:

- you want to generate content to come before the element contentn positionally
- The ::after content is also "after" in source order so it will position on top of ::before if stacked on top of each other natually.

***Note*** the content is still inside the element they are applied to. The naming sort of feels like they might come before or after the element. but it is really beofre or after *the other content inside*


The value of the `content` can be
- ***a string*** 
  - special characters need to be specially encoded as unicode entity
- ***an image***
  - `conten: url(path/to/image)`
  - The image is inserted at it's exact dimentsions and ***CAN NOT BE RESIZED***   
- ***Nothing***
  - Useful for clearfix and inserting images as backgroud images  
- ***A Counter***  

# ::marker

The ::marker pseudo-eleemnt is for styling the stylistic marker of a list element. For example, the bullet point of a default *ul* or the numeral of a default *ol*
If you change the display property to list-item on any element, you can contols its marker.

