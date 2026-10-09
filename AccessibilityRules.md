## CRITICAL ACCESSIBILITY RULESET


**Zero Page Speculation:** You have no visibility into the parent application DOM. Never predict, assume, or infer pre-existing element states, host structures.


### 1. Allowed ARIA Vocabulary & Mapping Behavior
When states update dynamically via interactive scripts, the associated ARIA attributes must update inline concurrently. You are permitted to evaluate and verify only the following ARIA categories within the local code scope:
* aria-selected
* aria-disabled
* aria-labeledby
* role
* aria-hidden
* aria-expanded
* aria-label
* aria-haspopup
* aria-modal
* aria-checked
* aria-controls
* aria-describedby
* aria-pressed
* aria-invalid
* aria-live


### 2. Tabindex & Focus Management
- When only a partial snippet is provided, do not infer missing DOM context, surrounding page structure, or hidden parent elements. Add tabindex only when the snippet itself clearly shows that a custom interactive element or non-native control must be keyboard reachable and is not already natively focusable.
- Preserve a logical tab order. Implement focus management only for the components present in the provided snippet.
- For modal dialogs and other focus-contained components, strictly move focus into the component when it opens, trap focus within it while it is active, and return focus to the triggering element when it closes and always implement keyboard focus trapping and ensure `Tab` and `Shift+Tab` cycle through the modal’s focusable elements only while it is active.
- For any custom interactive widget (including custom dropdowns, listboxes, menus, popups, and comboboxes), implement the entire focus movement, opening/closing behavior, focus trapping, selection, and focus restoration, allowing tab-based navigation and returning focus to the triggering element only when the component is dismissed through its close action (such as Escape or selecting an option).


### 3. Images and Form Labels
- Images must include an appropriate `alt` attribute.
- Form controls that have visible labels must be associated with a matching `for` attribute on the label.


### 4. Opacity
- If opacity: 0 is used to visually hide an element, ensure that the element is not unintentionally exposed to assistive technologies or left keyboard-focusable. If the element is intended to be completely hidden, use an appropriate technique such as display: none, visibility: hidden, or aria-hidden="true" wherever appropriate.
