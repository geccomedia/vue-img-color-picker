# vue-img-color-picker
Vue component to pick a color from a base64 image, by clicking on it.

You can access the selected color by $refs.colorPicker.color, or from the $emit event "setColor".
See Examples below.

Options:
ref: to access the color by $refs
width: width of the displayed image (apect ratio will be respected)
showColor: display selected color in a box at top right
initColor: if you need to pre define a selected color
imagesrc: the base64 encoded image (urls are not accepted because of cross origin problems)

``` html 
<img-color-picker
  ref="colorPicker"
  :width="400"
  :showColor="true"
  @setColor="setColor"
  :initColor="userColor"
  imagesrc="data:image/png;base64,...">
</img-color-picker>
```

setColor event handler in parent component:
``` js
setColor (color){
  console.log(color);
},
```
