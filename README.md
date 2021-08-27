
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

#CSS 
- Flexbox
- Float
- Table
- Grid
#HTML
#JavaScript
