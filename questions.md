
# 1.Button


### Shared Configurable Properties (Applies to all Button Subtypes)
- `Button text`: Subtype default (`'Primary button'`, `'Secondary button'`, or `'Link button'`)
- `size`: Subtype default (`'small'`, `'medium'`, or `'large'`)
- `disabled`: `false` (`true` or `false`)
- `include icon/image`: `false` (`true` or `false`)


## Variant Specific Configurable Properties


### Primary solid button, Secondary solid button
- `icon/image source`: `''` (configurable only when `include icon/image` is `true`; user can type path of image or code for SVG markup as 2 ways of input)


### Primary outlined button, Secondary outlined button
- `icon/image source before hover`: `''` (configurable only when `include icon/image` is `true`; user can type path of image or code for SVG markup as 2 ways of input)
- `icon/image source after hover`: `''` (configurable only when `include icon/image` is `true`; user can type path of image or code for SVG markup as 2 ways of input)
---


# 2.Modal


### Configurable Properties
- `include image`: `false` (`true` or `false`)
- `image path`: `''` (user can type path of image or url; configurable when `include image` is `true`)
- `Modal title`: `'Modal Header'` (Header text)
- `Modal content`: `'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis eu arcu turpis. Curabitur hendrerit molestie tortor ut blandit. Quisque vel mattis nisi, ac euismod sem. Cras ut justo sed enim fringilla vestibulum. Sed quam nunc, aliquam vitae egestas a, fringilla vitae sem. Vestibulum magna urna, gravida vel suscipit nec, bibendum et ipsum.'` (body text)
- `showCloseIcon`: `true` (`true` or `false`)
- `no of button`: `1` (`0`, `1`, or `2`)(Ask for the button component configuration for each button treating each button as a child component. eg: If no of buttons is 2, ask the configuration for all 2 buttons))


# 3.Button Group


### Configurable Properties
- `no of buttons in group` : `2` (`2` or `3`)
- `button name`: `button $no`(Ask for the button name for each button. eg: If no of buttons is 3, ask the button name for all 3 buttons)
