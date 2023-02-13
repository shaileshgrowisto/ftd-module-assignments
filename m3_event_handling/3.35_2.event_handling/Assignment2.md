Write a code to create a function having toggle behaviour between content and buttpn text by an event click handler using a component.

We will perform same steps we did in the previous assignment.

Only difference, we will do it using a component. Component allows you to repeat the functionality, with different content and text

Follow below instructions:

1. Create a function by name as `toggle` having void return type and a mutable boolean argument `flag` which will switch the value of the argument passed as mutable variable from `true` to `false` and `false` to `true`. This will control the rendering of your components whether to display the content of not on the webpage.

Your code should look like

```
-- void toggle(flag):
boolean $flag:

flag = !flag

```

2. Create a component with name as `toggle_component` having
   a. caption string field with name as `click_text`
   b. Add a mutable boolean flag as `open` which will control the visibility of the content
   c. Add a string `content` variable which will have the text which will be displayed on toggle event
   d. Add a `ftd.column` with padding as 10px
   e. Inside `ftd.column` add a text component using `ftd.text` and place the variable `click_text`. Add the `toggle` event listener to this text component
   f. Inside `ftd.column` add a text component using `ftd.text` and place the variable `content`
   g. Now add the `if` condition to the text component having `content` variable

Your code should look like

```
-- component toggle_component:
boolean $open: false
caption click_text:
string content:

-- ftd.column:
padding.px: 10

-- ftd.text: $toggle_component.click_text
$on-click$: $toggle($flag = $toggle_component.open)

-- ftd.text: $toggle_component.content
if: { $toggle_component.open }

-- end: ftd.column

-- end: toggle_component

```

3. Now we have created `toggle_component` component, we can use it as many times we want. Consider below sample code which will execute the same feature with same code but with different content.

```
-- toggle_component:
click_text: Click to toggle content 1
content: Im visible content 1

-- toggle_component:
click_text: Click to toggle the content 2
content: Im visible content 2

```

Once code is written, run it in your browser and validate the toggle event by clicking on text
