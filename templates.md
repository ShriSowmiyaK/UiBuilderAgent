# UI design Specification

This document defines the canonical specifications, defaults, and guidelines for all supported components.

---

# Primary Button

### Properties
| Property | Default Value | Description |
| :--- | :--- | :--- |
| `label` | `'Primary button'` | Button text |
| `size` | `'medium'` | `'small'`, `'medium'`, or `'large'` |
| `disabled` | `false` | `true` or `false` |

### Design and template specification
- **Base:** `.btn` (display: `inline-flex`, align-items: `center`, justify-content: `center`, width: `auto`, box-sizing: `border-box`, font-family: `inherit`, border-radius: `6px`, border: `1.5px solid transparent`, transition: `0.15s ease`)
- **Theme:** `.btn--primary` (background: `#2563eb`, color: `#ffffff`, border-color: `#2563eb`)
- **Focus:** `:focus-visible` (outline: `2px solid #2563eb`, offset: `2px`)
- **Hover/Active:** `:hover` (background: `#1d4ed8`, border-color: `#1d4ed8`), `:active` (transform: `scale(0.98)`)
- **Sizes:** 
  - `small`: padding: `6px 12px`, min-height: `32px`, font-size: `12px`
  - `medium`: padding: `10px 18px`, min-height: `40px`, font-size: `14px`
  - `large`: padding: `14px 24px`, min-height: `48px`, font-size: `16px`

---

# Secondary Button

### Properties
| Property | Default Value | Description |
| :--- | :--- | :--- |
| `label` | `'Secondary button'` | Button text |
| `size` | `'medium'` | `'small'`, `'medium'`, or `'large'` |
| `disabled` | `false` | `true` or `false` |

### Design and template specification
- **Base:** `.btn` (display: `inline-flex`, align-items: `center`, justify-content: `center`, width: `auto`, box-sizing: `border-box`, font-family: `inherit`, border-radius: `6px`, border: `1.5px solid #d1d5db`, transition: `0.15s ease`)
- **Theme:** `.btn--secondary` (background: `#ffffff`, color: `#374151`, border-color: `#d1d5db`)
- **Focus:** `:focus-visible` (outline: `2px solid #6b7280`, offset: `2px`)
- **Hover/Active:** `:hover` (background: `#f3f4f6`, color: `#111827`, border-color: `#9ca3af`), `:active` (background: `#e5e7eb`, transform: `scale(0.98)`)
- **Sizes:** 
  - `small`: padding: `6px 12px`, min-height: `32px`, font-size: `12px`
  - `medium`: padding: `10px 18px`, min-height: `40px`, font-size: `14px`
  - `large`: padding: `14px 24px`, min-height: `48px`, font-size: `16px`

---

# Modal

### Properties
| Property | Default Value | Description |
| :--- | :--- | :--- |
| `title` | `'Modal Title'` | Header text |
| `content` | `'This is the modal body content.'` | Main message or body text |
| `closeText` | `'Close'` | Label for dismiss button in footer |
| `showCloseIcon` | `true` | Show top-right '×' dismiss icon (`true` or `false`) |
| `hasBackdrop` | `true` | Show darkened background overlay (`true` or `false`) |

### Design and template specification
- **Backdrop:** `.modal-backdrop` (position: `fixed`, inset: `0`, width: `100vw`, height: `100vh`, background: `rgba(0, 0, 0, 0.5)`, display: `flex`, align-items: `center`, justify-content: `center`, opacity: `0`, visibility: `hidden`, transition: `opacity 0.2s ease, visibility 0.2s ease`, z-index: `1000`)
- **Backdrop Variant (No Overlay):** When `hasBackdrop: false`, apply `.modal-backdrop--transparent` (background: `transparent`, pointer-events: `none`). The `.modal-dialog` must maintain `pointer-events: auto`.
- **Backdrop Active:** `.modal-backdrop.is-open` (opacity: `1`, visibility: `visible`)
- **Container:** `.modal-dialog` (background: `#ffffff`, width: `100%`, max-width: `480px`, min-height: `220px`, box-sizing: `border-box`, border-radius: `8px`, box-shadow: `0 10px 25px rgba(0, 0, 0, 0.15)`, transform: `translateY(-10px)`, transition: `transform 0.2s ease`, overflow: `hidden`)
- **Container Active:** `.modal-backdrop.is-open .modal-dialog` (transform: `translateY(0)`)
- **Header:** `.modal-header` (display: `flex`, align-items: `center`, justify-content: `space-between`, padding: `16px 20px`, border-bottom: `1px solid #e5e7eb`)
- **Title:** `.modal-title` (font-size: `18px`, font-weight: `600`, color: `#111827`, margin: `0`)
- **Close Icon:** `.modal-close-icon` (background: `transparent`, border: `none`, width: `32px`, height: `32px`, display: `inline-flex`, align-items: `center`, justify-content: `center`, font-size: `22px`, line-height: `1`, color: `#6b7280`, cursor: `pointer`, padding: `4px`, border-radius: `4px`, transition: `background-color 0.15s ease, color 0.15s ease`)
- **Close Icon Hover:** `.modal-close-icon:hover` (background-color: `#f3f4f6`, color: `#111827`)
- **Close Icon Focus:** `.modal-close-icon:focus-visible` (outline: `2px solid #6b7280`, outline-offset: `2px`)
- **Body:** `.modal-body` (padding: `20px`, font-size: `14px`, line-height: `1.5`, color: `#4b5563`)
- **Footer:** `.modal-footer` (display: `flex`, align-items: `center`, justify-content: `flex-end`, padding: `14px 20px`, border-top: `1px solid #e5e7eb`, background: `#f9fafb`)
- **Footer Close Button:** Uses `.btn .btn--secondary` (outline: `2px solid #6b7280`, outline-offset: `2px` on `:focus-visible`)
- **Accessibility & Interactivity Specification (JS)**
    - Do not generate an opener or trigger button for the modal unless the user explicitly requests one.
    - Open and close modal on trigger of close button or icon.
    - Update ARIA attributes accordingly.
    - Manage focus, including focus trapping and returning focus.