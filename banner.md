# Banner
---
## Layout & Structural Architecture
The banner consists of the following nested hierarchy:
1. **Outer Wrapper**: Centers the banner in its layout container.
   - `width`: `90%`
   - `margin`: `2px auto`
   - `border-radius`: `4px`

2. **Banner Card / Container**:
   - `background-color`: `#F5F2EF`
   - Contains:
     - Top row dismissal container (aligned right)
     - Main content container

3. **Dismiss Row**:
   - `display`: `flex`
   - `justify-content`: `flex-end`
   - `max-height`: `24px`

4. **Main Content Container**:
   - `display`: `flex`
   - `align-items`: `center`
   - `position`: `relative`
   - `padding`: `0px 16px 16px 16px`[When no close icon is present `padding`: `16px 16px 16px 16px`]
   - `gap`: `8px`
   - `font-family`: `'Trust Hartford Sans', arial, sans-serif`
   - Contains:
     - Text & leading icon area (flex auto)
     - Action button (flexible alignment)

5. **Leading Section (Icon + Text Column)**:
   - `display`: `flex`
   - `align-items`: `flex-start`
   - `gap`: `8px`
   - `flex`: `1 1 auto`
   - `min-width`: `0`

6. **Content Text Column**:
   - `display`: `flex`
   - `flex-direction`: `column`
   - `gap`: `8px`
   - `flex`: `1 1 auto`
   - `min-width`: `768px` (desktop default)
---

## Visual & Typography Styles

### Visibility Rule
  - If `Include Icon` is `true`: Display the icon that is provided by the user within the banner.
  - When `Include Icon` is `false`: Do not display the icon within the banner.

### Leading Icon
- Any visual/contextual SVG or icon element.
- `width`: `20px`
- `height`: `20px`
- `min-width`: `20px`
- `min-height`: `20px`
- `fill`: `currentColor`
- `color`: `#1A1A1A`
- `padding-top`: `1.5px`

### Heading
- `font-family`: `'Trust Hartford Sans', arial, sans-serif`
- `font-size`: `16px`
- `font-weight`: `700`
- `line-height`: `1.4`
- `margin`: `0`
- `color`: `#1A1A1A`

### Body Paragraph
- `font-family`: `'Trust Hartford Sans', arial, sans-serif`
- `font-size`: `16px`
- `font-weight`: `400`
- `line-height`: `1.5`
- `margin`: `0`
- `color`: `#1A1A1A`

### Close / Dismiss Button
#### Visibility Rule
  - If `Include Close Icon` is `true`: Display the close icon.
  - When `Include Close Icon` is `false`: Do not display the close icon.
- `margin`: `2px`
- `margin-top`: `6px`
- `margin-right`: `6px`
- `width`: `24px`
- `height`: `24px`
- `padding`: `2px`
- `background`: `transparent`
- `border`: `0`
- `cursor`: `pointer`
- **Focus visible state**:
  - `outline`: `none`
  - `border-radius`: `2px`
  - `box-shadow`: `0 0 0 0.125rem rgb(255, 255, 255), 0 0 0 0.25rem rgb(254, 48, 130)`

#### Close Icon SVG Asset
Use the following SVG markup for the dismiss button:
<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none" style="pointer-events: none;">
  <path d="M0.839887 15.1602C0.955946 15.2763 1.10753 15.3331 1.25912 15.3331C1.40952 15.3331 1.56111 15.2763 1.67717 15.1602L8.00002 8.83737L14.3229 15.1602C14.4377 15.2763 14.5893 15.3331 14.7409 15.3331C14.8925 15.3331 15.0441 15.2763 15.1602 15.1602C15.3911 14.9293 15.3911 14.5539 15.1602 14.3229L8.8373 8.00008L15.1602 1.67723C15.3911 1.4463 15.3911 1.07207 15.1602 0.839948C14.928 0.609015 14.5538 0.609015 14.3229 0.839948L8.00002 7.16281L1.67717 0.839948C1.44624 0.609015 1.07082 0.609015 0.839887 0.839948C0.608954 1.07207 0.608954 1.4463 0.839887 1.67723L7.16274 8.00008L0.839887 14.3229C0.608954 14.5539 0.608954 14.9293 0.839887 15.1602Z" fill="#75013F"/>
</svg>

### Action Button Layout Constraint
- Visual button styles are inherited directly from `buttons,modals.md`.
- Ensure the button container respects:
  - `min-width`: `200px` (desktop)
  - `flex-shrink`: `0`
---

## Responsive Breakpoint Behavior
### Tablet (`max-width: 991px` and `min-width: 768px`)
- **Content Text Column**: Adjust `min-width` to `400px`.
### Mobile (`max-width: 767.98px`)
- **Main Content Container**:
  - `flex-direction`: `column`
  - `align-items`: `stretch`
  - `gap`: `16px`
- **Content Text Column**:
  - `min-width`: `auto`
- **Action Button**:
  - `width`: `100%`
  - `min-width`: `0`
---

## Interactivity Specification (JS)
- Include close icon only when `close icon` value chosen `yes`.
- **Dismiss via Close Icon**: Clicking the close icon hides the banner.