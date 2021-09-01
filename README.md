
<!---
QDCSLG/QDCSLG is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

- Microsoft Ergonomic Keyboard 4000
  - How to change the zoom key to scroll up or down
  - [MS Mouse and Keyboard center](https://support.microsoft.com/en-us/topic/mouse-and-keyboard-center-download-f5b10905-7887-eedb-2f1c-d0737a36a3b2)
  - Follow instruction [here](https://superuser.com/questions/195474/change-zoom-action-to-scroll-in-a-ms-natural-keyboard-4000)
  
  Add the following section to the bottom of the commands.xml 
  
  ```xml
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

[Box-sizing css property description](https://github.com/QDCSLG/QDCSLG/blob/6b3aa2d17cc3bbc589c94274e3c9891cae3a32c1/box-sizing.md)

[Google Map Filter Popup](GoogleMapPopup.md)
# HTML

## What is the different between HTML properties and attributes

***HTML*** is the standard language for creating documents that are intended to be displayed on the web browser

***DOM*** short for *Document Object Model* When browser parses the HTML, it creates the DOM node based on the HTML code.

Attrinutes are defined in HTML, Properties are accessed from DOM nodes

When writing HTML code, you can define attributes on your HTML elements. Once the browser sees the code, it will parse the HTML and build a tree structure in memory to represent this HTML code. Once the element is converted into a node, node is an object there for it has properties.

- Few HTML attributes have 1:1 mapping for properties for example `id`
- Some HTML attributes don't have corresponding properties for example `aria-*`
- Some DOM properties don't have any attributes mapping, for example `textContent`

```
<input id="inputId" type="number" value="Name:">
```
For the above HTML markup, there are three attributes

- id
  - it is a `reflected` property. Getting the property reads the attributes value and set the property write the attrinute value
  - when use javascript code to modify the property, the HTML attribute will also change
- type
  - it is a `reflected` property
  - same thing for id
- value
  - it is also a `reflected` proeprty. But since it is editable by end user, thus it can be different when the dom is parsed from HTML and when the node is read
  - for example, after the page is load, modify the text box to anything other than the initial value
  - `element.getAttribute('value')` will return the initial value here `Name:`
  - `element.value` will return the current value in the control

  So properties contains the latest value of the node in DOM structure.
  Attributes contains the data when the HTML string is parsed. 

  Pretty good different here.

# JavaScript
