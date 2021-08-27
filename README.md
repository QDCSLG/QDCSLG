
<!---
QDCSLG/QDCSLG is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

- Microsoft Ergonomic Keyboard 4000
  - How to change the zoom key to scroll up or down
  - [MS Mouse and Keyboard center (https://support.microsoft.com/en-us/topic/mouse-and-keyboard-center-download-f5b10905-7887-eedb-2f1c-d0737a36a3b2)]
  - Follow instruction [here(https://superuser.com/questions/195474/change-zoom-action-to-scroll-in-a-ms-natural-keyboard-4000)]
  
  Add the following section to the bottom of the commands.xml 
  
  ```
  <Application UniqueName="MozillaWindowClass" AppName="Netscape">
    <C319 Type="6" Activator="ScrollUp" />
    <C320 Type="6" Activator="ScrollDown" />            
  </Application>
   ```

# CSS 
- Flexbox
- Float
- Table
- Grid

## `box-sizing` sets how the total width and height of an element is calculated
By default in the css box model, the `width` and `height` you assign to an element is applied only to the element's content box. If the elelemtn has any border or padding, this is then added to the `width` and `height` to arrive at the size of the box that's redered on the screen. This mneans that when you set the `width` and `height` you have to adjust the value you give to allow for any border or padding that may be added. For example, if you want four boxes with `width:25%`, if any has left or right padding or a left or right border, this will not by default fit on one line wihtin the constraints of parent container

`box-sizing` property can be used to adjust this behavior
- `content-box` gives you the default css box-sizing behavior, if you set the width to be 100px, then the elemetn's content box will be 100px width, and the width of any border or padding will be added to the final rendered width, making the element wider than 100px
  - When using `position:relative' or `position:absolute` using of `box-sizing:content-box` allows the positioning values to be relative to the content and independent of changes to border and padding sizes which is sometimes desirable.
  -  
- border-box tells the browser to account for any border and padding in the values you specify for an element's width and height. If you set an element's width to be 100px, that 100px will include any order or padding you added, and the content box will shrink to absorb that extra width, this typically make is much easier to size element. `box-sizing:border-box` is the default styling that broswer use for 
 - table
 - select
 - button
 - input
   - radio
    -checkbox
    - reset
    - button
    - submit
    - color
    - search 

**Note:** For layout, it is often userfurl to use `box-sizing:border-box` This makes dealing with the sizes of elements much easier and generally eliminate a number of pitfalls you can stumble on while laying out your content. On the other hand

### Formal Definition
- Initial value
  - content-box   
- Applies to
  - all elements that accept width or height 

### Example
 **HTML**
 ```
 <div class="content-box">Content box</div>
<br>
<div class="border-box">Border box</div>
 ```
 ***CSS***
```
div {
  width: 160px;
  height: 80px;
  padding: 20px;
  border: 8px solid red;
  background: yellow;
}

.content-box {
  box-sizing: content-box;
  /* Total width: 160px + (2 * 20px) + (2 * 8px) = 216px
     Total height: 80px + (2 * 20px) + (2 * 8px) = 136px
     Content box width: 160px
     Content box height: 80px */
}

.border-box {
  box-sizing: border-box;
  /* Total width: 160px
     Total height: 80px
     Content box width: 160px - (2 * 20px) - (2 * 8px) = 104px
     Content box height: 80px - (2 * 20px) - (2 * 8px) = 24px */
}

```
***Result***
![image](https://user-images.githubusercontent.com/12564206/131061567-8d55c183-7904-440a-a917-0bc168ba2f5a.png)

In [bootstrap source code (https://github.com/twbs/bootstrap/blob/main/scss/_reboot.scss)], one of the first line of code is to set everthing to border-box
Same thing as tailwindcss
```
// Document
//
// Change from `box-sizing: content-box` so that `width` is not affected by `padding` or `border`.

*,
*::before,
*::after {
  box-sizing: border-box;
}

```

# HTML
# JavaScript
