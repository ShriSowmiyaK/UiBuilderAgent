# Button


### Shared Design Specification


#### Base Layout
`display`: `block`, `text-align`: `center`, `user-select`: `none`, `border`: `1px solid`, `cursor`: `pointer`, `margin`: `0`, `font-family`: `'Trust Hartford Sans', arial, sans-serif`, `line-height`: `1.5`, `border-radius`: `0.25rem`, `font-weight`: `700`, `min-width`: `200px`


#### Icon / Image
`display`: `inline-block`, `vertical-align`: `middle`


- If `include icon` is `true` for `solid primary button`, `solid secondary button`:
  - The SVG color must not be changed. If the SVG does not contain any color then it must inherit the button text color.


- If `include icon` is `true` for `primary outlined button`, `secondary outlined button`:
  - The SVG must always inherit the button's text color. If the SVG is provided with hardcoded colors (e.g., `fill="..."` or `stroke="..."`), or lacks color attributes, replace or set the relevant color property to `currentColor` (e.g., `fill="currentColor"` or `stroke="currentColor"` depending on the SVG type).


* If the `icon position` is `left`, then the icon appears first followed by the button text. If `icon position` is `right`, then the button text appears first followed by the icon.


#### Responsive Sizing


##### Small Button
`padding`: `4px 8px 4px 8px`, `font-size`: `14px`, `line-height`: `1.5`, `icon width`: `16px`, `icon height`: `16px`  
* Mobile (< 768px):  
  `width`: `100%`


##### Medium Button
`padding`: `7px 12px 7px 12px`, `font-size`: `16px`, `icon width`: `18px`, `icon height`: `18px`  
* Mobile (< 768px):  
  `width`: `100%`


##### Large Button
* Desktop & Tablet (≥ 768px):  
  `padding`: `8px 16px 8px 16px`, `font-size`: `18px`, `icon width`: `20px`, `icon height`: `20px`  
* Mobile (< 768px):  
  `width`: `100%`


#### Disabled State (General)
`cursor`: `not-allowed`, `opacity`: `1`, `box-shadow`: `none`, `color`: `#6B6B6B`


---


## 1. Primary Button


### Default Property Overrides
- `Button text`: `'Primary button'`
- `size`: `'medium'`


### Specific Styling
`focus-box-shadow`: `0 0 0 0.125rem rgb(255, 255, 255), 0 0 0 0.25rem rgb(254, 48, 130)`


#### Variant 1: Solid primary button:
`color`: `#ffffff`, `bg`: `#75013F`, `border-color`: `#75013F`, `hover-color`: `#ffffff`, `hover-bg`: `#5e0132`, `hover-border-color`: `#58012f`, `focus-shadow-rgb`: `138, 39, 92`, `active-color`: `#ffffff`, `active-bg`: `#52012c`, `active-border-color`: `#4c0129`, `active-shadow`: `inset 0 3px 5px 0 rgba(0, 0, 0, 0.13)`, `disabled-color`: `#ffffff`, `disabled-bg`: `#75013F`, `disabled-border-color`: `#75013F`


##### Variant 2: Outlined primary button:
`bg`: `transparent`, `border-width`: `1px`, `box-shadow`: `inset 0 0 0 0 rgba(0, 0, 0, 0)`, `disabled-opacity`: `0.65`, `color`: `#75013F`, `border-color`: `#75013F`, `hover-color`: `#ffffff`, `hover-bg`: `#75013F`, `hover-border-color`: `#75013F`, `focus-shadow-rgb`: `117, 1, 63`, `active-color`: `#ffffff`, `active-bg`: `#75013F`, `active-border-color`: `#75013F`, `active-shadow`: `inset 0 3px 5px 0 rgba(0, 0, 0, 0.13)`, `disabled-color`: `#75013F`, `disabled-bg`: `transparent`, `disabled-border-color`: `#75013F`


---


## 2. Secondary Button


### Default Property Overrides
- `Button text`: `'Secondary button'`
- `size`: `'medium'`


### Specific Styling
`focus-box-shadow`: `0 0 0 0.125rem rgb(255, 255, 255), 0 0 0 0.25rem rgb(254, 48, 130)`


#### Variant 1: Solid secondary button:
`color`: `#ffffff`, `bg`: `#181818`, `border-color`: `#181818`, `hover-color`: `#ffffff`, `hover-bg`: `#131313`, `hover-border-color`: `#121212`, `focus-shadow-rgb`: `59, 59, 59`, `active-color`: `#ffffff`, `active-bg`: `#111111`, `active-border-color`: `#101010`, `active-shadow`: `inset 0 3px 5px 0 rgba(0, 0, 0, 0.13)`, `disabled-color`: `#ffffff`, `disabled-bg`: `#181818`, `disabled-border-color`: `#181818`


##### Variant 2: Outlined secondary button:
`bg`: `transparent`, `border-width`: `1px`, `box-shadow`: `inset 0 0 0 0 rgba(0, 0, 0, 0)`, `color`: `#181818`, `border-color`: `#181818`, `hover-color`: `#ffffff`, `hover-bg`: `#181818`, `hover-border-color`: `#181818`, `focus-shadow-rgb`: `24, 24, 24`, `active-color`: `#ffffff`, `active-bg`: `#181818`, `active-border-color`: `#181818`, `active-shadow`: `inset 0 3px 5px 0 rgba(0, 0, 0, 0.13)`, `disabled-color`: `#181818`, `disabled-bg`: `transparent`, `disabled-border-color`: `#181818`


---


## 3. Link Button


### Default Property Overrides
- `Button text`: `'Link button'`
- `size`: `'medium'`


### Specific Styling
`background-color`: `transparent`, `border`: `none`, `border-color`: `transparent`, `box-shadow`: `none`, `color`: `#1570be`


* Hover: `color`: `#23527c`, `text-decoration`: `underline`, `background-color`: `transparent`
* Focus: `color`: `#23527c`, `text-decoration`: `underline`, `background-color`: `transparent`, `outline`: `0.125em solid #1570be`, `box-shadow`: `0 0 0.063em 0.25em #c8e1ff`
* Disabled:  
  Hover: `color`: `#6B6B6B`, `text-decoration`: `none`


---


# Modal


### Design and Template Specification


#### Modal Backdrop
`position`: `fixed`, `top`: `0`, `right`: `0`, `bottom`: `0`, `left`: `0`, `z-index`: `1050`, `background-color`: `rgba(0,0,0,0.6)`, `opacity`: `0`, `display`: `flex`, `align-items`: `flex-start`, `justify-content`: `center`


#### Modal Content container
`position`: `relative`, `display`: `flex`, `align-items`: `center`  
`background-color`: `#ffffff`, `border top`: `6px solid #e1d8cf`, `padding`: `22px`, `margin`: `5px 0px 10px 0px`  
* Desktop (≥ 992px): `width`: `700px`  
* Tablet (≥ 768px): `width`: `600px`  
* Mobile (< 768px): `width`: `auto`


* Only when the modal includes a top image: stack the image, header, body, and footer vertically and center them horizontally. Apply `flex-direction`: `column`, `align-items`: `center`, and `text-align`: `center` to the modal content container; keep the close icon absolutely positioned at the top-right. Without an image, retain the default layout and alignment.


#### Close Icon (icon within a button)
`position`: `absolute`, `top`: `15px`, `right`: `15px`, `z-index`: `1`, `display`: `inline-flex`, `align-items`: `center`, `justify-content`: `center`, `width`: `24px`, `height`: `24px`, `padding`: `0`, `border`: `0`, `background`: `transparent`, `cursor`: `pointer`, `opacity`: `1`, `filter`: `drop-shadow(0 1px 0 #ffffff)`, `svg markup to be used`: `<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none" style="pointer-events: none;"><path d="M0.839887 15.1602C0.955946 15.2763 1.10753 15.3331 1.25912 15.3331C1.40952 15.3331 1.56111 15.2763 1.67717 15.1602L8.00002 8.83737L14.3229 15.1602C14.4377 15.2763 14.5893 15.3331 14.7409 15.3331C14.8925 15.3331 15.0441 15.2763 15.1602 15.1602C15.3911 14.9293 15.3911 14.5539 15.1602 14.3229L8.8373 8.00008L15.1602 1.67723C15.3911 1.4463 15.3911 1.07207 15.1602 0.839948C14.928 0.609015 14.5538 0.609015 14.3229 0.839948L8.00002 7.1628L1.67717 0.839948C1.44624 0.609015 1.07082 0.609015 0.839887 0.839948C0.608954 1.07207 0.608954 1.4463 0.839887 1.67723L7.16274 8.00008L0.839887 14.3229C0.608954 14.5539 0.608954 14.9293 0.839887 15.1602Z" fill="#75013F"/></svg>`


#### Top Image (Above Header)
`display`: `block`, `margin`: `0 auto 15px auto`  
* Desktop (≥ 992px): `max-width`: `200px`, `max-height`: `200px`  
* Tablet (768px to 991px): `max-width`: `150px`, `max-height`: `150px`  
* Mobile (< 768px): `max-width`: `120px`, `max-height`: `120px`


#### Modal Header
`padding-bottom`: `12px`, `font-size`: `24px`, `line-height`: `1.2`, `font-weight`: `700`, `color`: `#75013f`, `font-family`: `Trust Hartford Sans, Times New Roman`


#### Modal Body
`position`: `relative`, `font-size`: `16px`, `line-height`: `1.5em`, `color`: `#1a1a1a`, `font-weight`: `400`, `margin-bottom`: `20px`, `font-family`: `Trust Hartford Sans, arial, sans-serif`


#### Modal Footer Container
`padding-top`: `1.429em`, `border-top`: `0`, `padding-bottom`: `0`, `margin-left`: `auto`, `margin-right`: `auto`  
* Desktop & Tablet (≥ 992px): `display`: `flex`, `flex-direction`: `row`, `flex-wrap`: `wrap`, `align-items`: `center`, `gap`: `10px`, `justify-content`: `center`  
* Mobile (< 768px): `width`: `calc(100% + 20px)`, `margin-left`: `-10px`, `margin-right`: `-10px`, `display`: `flex`, `flex-direction`: `column`, `gap`: `10px`


#### Footer Buttons (held as individual buttons inside Modal Footer Container):
* Tablet/mobile (≤ 768px): `width`: `100%`


### Interactivity Specification (JS)
- Do not generate an opener or trigger button for the modal.
- The modal must not close on click of the backdrop.
- If both `showCloseIcon` is `false` and no dismiss buttons exist inside the modal, omit JavaScript and display the modal open directly.
- For each configured modal button, if the agent identifies that the button semantically conveys a dismissal or exit intent (such as closing, cancelling, backing out, or dismissing), then automatically attach the dismissal JavaScript handler so that clicking it closes the modal. Strictly do not rely on hardcoded literal matches, simply attach javascript handler when the intent indicates close and never treat disabled buttons as dismiss triggers.
- When include image is true, render the image centered above the header. The close icon (`showCloseIcon`), when true, must be anchored directly at the top-right corner within the Modal Content container above the image—not placed inline or beside the header title.
