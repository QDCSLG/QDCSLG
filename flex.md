# A complete guide to Flexbox

Reading notes from this [document](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#background) on css-tricks

## What is Flexbox

The `Flexbox layout` modeul amins at providing a more efficient way to lay out, align and distrute space among items in a container, even when their size is unknown or dynamic (Thus the word "flex")

The main idea behind the flex layout is to gibe the container the ability to alter its items widht/height and order to best fill the availble space (Mostly to accommodate to all kind of display devices and screen sizes.) A flex container expands items to fill availble free space or shrinks them to prevent overflow.

Most importantly, the flexbox layout is direction agnostic as opposed to the regular layouts (block which is vertically-based and inline which is horizontally-based.) While those work well for pages, they lack flexibility  to support large or complex applications (especially when it comes to orientation changing, resizing, stretching, shrinking and etc)

*Note* Flexbox layout is most appropriate to the components of an application and small-scale  layouts, while the Grid layout is intended for larger scale layouts.
Small or large is really depends on each application. Since we are using Bootstrap 4, Flex is probably going to be the way to go.

## Basics and terminology

Since flexbox is a whole module and not a single property, it invovles a lot of things including its whole set of properties. Some of them are meant to be set on the container (parent element, known as "flex container") whereas the others are meant to set on the children (said "flex items")

If "regular" layout is based on both block and inline flow directions, the flex layout is based on "flex-flow directions" Pleae have a look at this firugre from the specification, explaining the main idea behind the main idea behind the flex layout.

Items will be laied out following either the *main axis* (from main-start to main-end) or the cross-axis (from cross-start to cross-end).

- Main axis
  - the main axis of the flex container is the primary axis along which flex items are laid out. 
  - Beware, it is not necessarily horizontal; it depends on the `flex-direction` property

- Cross axis
  - the axis perpendicular to the main axis is called the cross axis. Its direction depends on the main axis direction.

 ## Flexbox properties

 - Properties for container (Parent)
   - display
     - this defines a flex container. Inline or block depending on the given value. It enables a flex context for all its direct children.
     - Choices
       - flex
       - inline-flex
    - Not the css columns have no effect on a flex container.
- flex-direction
  - this establishes the main-axies. Thus defining the direction flex items are placed in the flex container. Flexbox is (aside from optional wrapping) a single-direction layout concept. Think of flex item as primarily laying out either in horizontal rows or vertical columns
  - choices
    - row
    - row-reverse
    - column
    - colum-reverse






# Sample layout

```
 <div id="mmenu_screen" class="vh-100 container-fluid main_container d-flex">
        <div class="row flex-fill">
            <div class="col-sm-6 h-100">
                <div class="row h-50">
                    <div class="col-sm-12" id="mmenu_screen--book">
                        <!-- Button for booking -->
                        Booking
                    </div>
                </div>
                <div class="row h-50">
                    <div class="col-sm-12" id="mmenu_screen--information">
                        <!-- Button for information -->
                        Info
                    </div>
                </div>
            </div>
            <div class="col-sm-6 mmenu_screen--direktaction flex-fill">
                <!-- Button for direktaction -->
                Action
            </div>
        </div>
    </div>
    ```