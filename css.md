# CSS

## What is the difference between position relative, absolute and fixed?

- Relative - the element is positioned relative to its normal position.
- Absolute - the element is positioned absolutely to its first positioned parent.
- Fixed - the element is positioned related to the browser window.

Here is an [example](https://codepen.io/bonnieli/pen/OJMRYxG)

## What are ways you can make elements visually hide content and only make it available for screen readers?

Screen readers use the DOM order of elements to decide what to read first, so be sure to order HTML elements for logical content flow regardless of CSS positioning.

#### Do

- Use `position: absolute` to move content, placing it relative to a parent component, and keeping the page flow for screen readers.

A helper class is commonly used to position the content.
- One method is to position the content offscreen to the left. You can also resize the content so that it is very small if positioning is disabled.
- Another method is to use resizing and `clip-path` to hide the element
*Note: some browsers may better support `clip` from CSS2*

```
.screenreader-only{
    position:absolute;

    /*offscreen and to the left of parent element*/
    /*left:-10000px;*/

    /*resizes element, hides text or content that overflows*/
    width:1px;
    height:1px;
    overflow:hidden;

    /*clip element*/
    clip: rect(1px 1px 1px 1px);  /*IE 6 and 7*/
    clip: rect(1px,1px,1px,1px);
    clip-path: polygon(0px 0px, 0px 0px, 0px 0px);
    -webkit-clip-path: polygon(0px 0px, 0px 0px, 0px 0px);
}
```

- Also utilize aria-labels, alt text, html best practices and library built ins for descriptive labeling of elements

For example, providing a unique `id` for a `Textfield` component in Material-UI will link the input to its label and helper text [Material-UI docs](https://material-ui.com/components/text-fields/#accessibility)

#### Don't

- Use `visibility:hidden` or `display:none` unless you want it hidden visually *and* hidden from screen readers
- Set width and height to zero, this would take the element out of the page flow (will be ignored by screen readers)
- Set font size or line height to zero, may be interpreted as malicious and affect SEO (search engine optimization)

More info: [webaim](https://webaim.org/techniques/css/invisiblecontent/) , [accessible360](https://accessible360.com/accessible360-blog/use-aria-label-screen-reader-text/) , [stackoverflow](https://stackoverflow.com/questions/26032089/in-html-how-can-i-have-text-that-is-only-accessible-for-screen-readers-i-e-fo)
