Write a code to create a function having toggle behaviour between content by an event click handler.

Follow below instructions to create a event handler which will toggle your content:

1. Create a function by name as `toggle` having void return type and a mutable boolean argument `flag` which will switch the value of the argument passed as mutable variable from `true` to `false` and `false` to `true`. This will control the rendering of your components whether to display the content of not on the webpage.

Your code should look like

```
-- void toggle(flag):
boolean $flag:

flag = !flag

```

2. Now create two toggle text by using `ftd.text`
   a. First Text as `Click me to toggle the content` and attach the toggle event on the FTD component using `on-click` event handler.
   b. Second Text as `Im visible content now` which wil have a `if` conditional attribute

3. You have to create a mutable boolean variable outside the event handler which will be passed as the reference so that the value switched is synced and we get the functionality workd. Lets create a mutable variable for this by name as `open` and having default value as `false`

Your code should look like:

```
-- boolean $open: false

-- ftd.text: Click me to toggle the content
$on-click$: $toggle($flag = $open)

-- ftd.text: Im visible content now
if: { open }

```

Once done, run this code in your browser and validate the toggle event by clicking on text `Click me to toggle the content`
