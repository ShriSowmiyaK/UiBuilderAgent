# Toggle Button


#### Container Layout (Parent `<div>`)
`display` : `flex`, `flex-wrap` : `nowrap`, `width` : `80%`


#### Button Item (`<div>` child buttons)
`display` : `block`, `flex` : `1 1 0`, `width` : `50%`, `padding` : `8px 16px`, `font-size` : `16px`, `font-weight` : `400`, `line-height` : `1.25em`, `text-align` : `center`, `vertical-align` : `middle`, `color` : `#1a1a1a`, `background-color` : `#ffffff`, `border` : `1px solid #1a1a1a`, `cursor` : `pointer`, `user-select` : `none`, `box-sizing` : `border-box`, `font-family` : `Trust Hartford Sans, arial, sans-serif`


* Desktop & Tablet (≥ 768px):
`flex` : `0 0 auto`, `width` : `auto`, `min-width` : `160px`


#### Hover State
`border-color` : `#75013F`, `border-color` : `#75013F`, `color` : `#1a1a1a`


#### Selected State (`.is-selected`)
`box-shadow` : `inset 0 3px 7px rgba(0, 0, 0, 0.47)`, `color` : `#ffffff`, `background-color` : `#1a1a1a`


# Radio Button Group


#### Container Layout (Parent)
`display` : `flex`, `flex-direction` : `column`, `border` : `none`, `padding` : `0`, `margin` : `0`


#### Radio Option Item (`wrapper of input and label`)
`display` : `flex`, `margin-top` : `10px`, `margin-bottom` : `10px`, `font-family` : `Trust Hartford Sans, arial, sans-serif`, `font-size` : `16px`, `font-weight` : `400`, `line-height` : `1.4`, `cursor` : `pointer`, `user-select` : `none`


#### Radio Input Control
`cursor` : `pointer`, `margin` : `0 10px 0 0`, `width` : `21px`, `height` : `21px`, `color` : `#1A1A1A`


#### Label Text (`<span>` inside the option)
`padding-bottom` : `3px`, `line-height` : `inherit`, `color` : `#1A1A1A`
