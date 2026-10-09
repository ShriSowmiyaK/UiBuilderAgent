# Button Group


#### Container Layout (Parent `<div>`)


`display`: `flex`, `flex-wrap`: `nowrap`, `width`: `80%`


#### Button Item (`<div>` child buttons)


`display`: `block`, `flex`: `1 1 0`, `width`: `50%`, `padding`: `8px 16px`, `font-size`: `16px`, `font-weight`: `500`, `line-height`: `1.25em`, `text-align`: `center`, `vertical-align`: `middle`, `color`: `#3a5a78`, `background-color`: `#ffffff`, `border`: `1px solid #3a5a78`, `cursor`: `pointer`, `user-select`: `none`, `box-sizing`: `border-box`, `transform`: `scale(1)`, `z-index`: `2`


* Desktop & Tablet (≥ 768px):
`flex`: `0 0 auto`, `width`: `auto`, `min-width`: `160px`


#### Hover State


`border-color`: `#4e79a2`, `box-shadow`: `0 0 2px 2px rgba(36, 119, 191, 0.5)`


#### Focus State
* focus state (for mouse focus).`
For mouse focus (:focus:not(:focus-visible)):
background-color: #4e79a2, border-color: #3a5a78, color: #ffffff, outline: none, box-shadow: inset 0 3px 7px rgba(0, 0, 0, 0.47)


* For keyboard focus (when pressing tab, :focus-visible):
background-color: #ffffff, border-color: #4e79a2, color: #3a5a78, outline: none, box-shadow: 0 0 2px 2px rgba(36, 119, 191, 0.5)
