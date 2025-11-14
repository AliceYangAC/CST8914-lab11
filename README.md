# Lab 11: Accessible Custom Components & Widgets

## Questions

1. What is the keyboard interaction missing?

They keyboard cannot move focus to the next header with "Down Arrow" or back to previous accordion header with "Up Arrow." However, this is optional; the accordion component does have the main keyboard interactions required:

- `Space` or `Enter`: when focus is on the accordion header element of a collapsed section, expands the section and vice versa.
- `Tab`: moves focus to next focusable element; all focusable elements in accordion are in the page `Tab` sequence
- `Shift + Tab`: moves focus to the previous focusable element; all focusable elements in accordion are in the page `Tab` sequence

2. What is the ARIA missing?

- `aria-expanded="true"`: The accordion header element (button) needs this ARIA to establish the state when the accordian panel is expanded (true) or closed (false).

- `aria-controls="ID"`: This identifies the accordion panel that this button accordion header controls.

- `role="region"`: This defines the accordion panel container (div) as a landmark region that contains the currently expanded accordion panel. This is critical for identifying the structure of a web page, and allows screen readers to provide keyboard navigation to important sections in a page.

- `aria-labelledby="IDREF"`: This references back to the accordion header element (button) that expands and collapses this accordion panel container, (div) which is critical for screen readers to understand the relationship between the accordion header and panel.