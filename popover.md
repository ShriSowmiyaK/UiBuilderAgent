# Popover


### Design and Layout Specification


#### page container
`min-height` : `100vh`, `display` : `flex`, `justify-content` : `center`, `align-items` : `center`


#### Popover Anchor Wrapper
`position` : `relative`, `display` : `inline-block`


#### Popover Container (Base / Shared)
`display` : `none`, `position` : `absolute`, `max-width` : `320px`, `box-sizing` : `border-box`, `background` : `#ffffff`, `border` : `1px solid rgba(0, 0, 0, 0.2)`, `border-top` : `6px solid #e1d8cf`, `box-shadow` : `0 0 10px rgba(0, 0, 0, 0.75)`, `padding` : `16px`, `color` : `#000000`, `font-family` : `Trust Hartford Sans, arial, sans-serif`, `line-height` : `1.42857`, `font-size` : `16px`, `font-weight` : `300`, `z-index` : `1000`


**Active / Visible State**:
`display` : `block`


---


### Directional Placements & Arrows


#### 1. Top Placement (Default)
Popover appears **above** the button; arrow sits at the bottom edge pointing **down** toward the button.


**Container Positioning**:
`bottom` : `calc(100% + 11px)`, `top` : `auto`, `left` : `50%`, `right` : `auto`, `transform` : `translateX(-50%)`


**Arrow Pointer (::after)**:
`content` : `""`, `position` : `absolute`, `bottom` : `-10px`, `top` : `auto`, `left` : `50%`, `right` : `auto`, `margin-left` : `-10px`, `margin-top` : `0`, `display` : `block`, `width` : `0`, `height` : `0`, `border-style` : `solid`, `border-width` : `10px 10px 0 10px`, `border-color` : `transparent`, `border-top-color` : `#ffffff`


#### 2. Bottom Placement
Popover appears **below** the button; arrow sits at the top edge pointing **up** toward the button.


**Container Positioning**:
`top` : `calc(100% + 11px)`, `bottom` : `auto`, `left` : `50%`, `right` : `auto`, `transform` : `translateX(-50%)`


**Arrow Pointer (::after)**:
`content` : `""`, `position` : `absolute`, `top` : `-16px`, `bottom` : `auto`, `left` : `50%`, `right` : `auto`, `margin-left` : `-10px`, `margin-top` : `0`, `display` : `block`, `width` : `0`, `height` : `0`, `border-style` : `solid`, `border-width` : `0 10px 10px 10px`, `border-color` : `transparent`, `border-bottom-color` : `#ffffff`


#### 3. Left Placement
Popover appears **to the left** of the button; arrow sits on the right edge pointing **right** toward the button.


**Container Positioning**:
`top` : `50%`, `bottom` : `auto`, `right` : `calc(100% + 11px)`, `left` : `auto`, `transform` : `translateY(-50%)`


**Arrow Pointer (::after)**:
`content` : `""`, `position` : `absolute`, `top` : `50%`, `bottom` : `auto`, `right` : `-10px`, `left` : `auto`, `margin-top` : `-10px`, `margin-left` : `0`, `display` : `block`, `width` : `0`, `height` : `0`, `border-style` : `solid`, `border-width` : `10px 0 10px 10px`, `border-color` : `transparent`, `border-left-color` : `#ffffff`


#### 4. Right Placement
Popover appears **to the right** of the button; arrow sits on the left edge pointing **left** toward the button.


**Container Positioning**:
`top` : `50%`, `bottom` : `auto`, `left` : `calc(100% + 11px)`, `right` : `auto`, `transform` : `translateY(-50%)`


**Arrow Pointer (::after)**:
`content` : `""`, `position` : `absolute`, `top` : `50%`, `bottom` : `auto`, `left` : `-10px`, `right` : `auto`, `margin-top` : `-10px`, `margin-left` : `0`, `display` : `block`, `width` : `0`, `height` : `0`, `border-style` : `solid`, `border-width` : `10px 10px 10px 0`, `border-color` : `transparent`, `border-right-color` : `#ffffff`


---


### Popover Inner Elements


#### Popover Header
`margin` : `0`, `padding` : `0 1.375em 1em 0`, `font-size` : `20px`, `font-weight` : `500`, `color` : `#75013f`, `font-family` : `Trust Hartford Sans, arial, sans-serif`


#### Popover Body / Content
`font-size` : `16px`, `text-align` : `start`, `line-height` : `1.4`, `font-family` : `Trust Hartford Sans, arial, sans-serif`, `font-weight` : `300`, `font-color` : `#1a1a1a`


---


### Close Icon
`position` : `absolute`, `top` : `16px`, `right` : `16px`, `width` : `24px`, `height` : `24px`, `cursor` : `pointer`, svg markup to be used : `<svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 16 16" fill="none" style="pointer-events: none;"><path d="M0.839887 15.1602C0.955946 15.2763 1.10753 15.3331 1.25912 15.3331C1.40952 15.3331 1.56111 15.2763 1.67717 15.1602L8.00002 8.83737L14.3229 15.1602C14.4377 15.2763 14.5893 15.3331 14.7409 15.3331C14.8925 15.3331 15.0441 15.2763 15.1602 15.1602C15.3911 14.9293 15.3911 14.5539 15.1602 14.3229L8.8373 8.00008L15.1602 1.67723C15.3911 1.4463 15.3911 1.07207 15.1602 0.839948C14.928 0.609015 14.5538 0.609015 14.3229 0.839948L8.00002 7.16281L1.67717 0.839948C1.44624 0.609015 1.07082 0.609015 0.839887 0.839948C0.608954 1.07207 0.608954 1.4463 0.839887 1.67723L7.16274 8.00008L0.839887 14.3229C0.608954 14.5539 0.608954 14.9293 0.839887 15.1602Z" fill="#75013F"/></svg>`


### Trigger Button Specification
Apply the chosen button variant and sizing directly from `buttons-modal.md` using its shared base layout, responsive sizes, its configurations and state definitions. Also apply the below mentioned style.


For mobile view(<768px) : `width` : `fit-content`


### Interactivity Specification (JS)
**Toggle Visibility**: Clicking the trigger button alternates the active visibility state of the popover container and stops event propagation.


**Dismiss via Close Icon**: Clicking the close icon hides the popover container.
