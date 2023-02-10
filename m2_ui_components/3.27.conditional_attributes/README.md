Write a code to create component having caption title and with a boolean flag through which we will handle the conditional attributes of the component.

Previously we conditionally handled the components, now we will handled the attributes on conditions

Follow below instructions to write the code:

1. Create a boolean flag with name as `present` and value as true

2. Create a component with name as `display` having
   a. caption string field with name as `title`
   b. Pass the caption title to `ftd.text` like `$display.title`
   c. Now pass the color value using `$inherited.colors.text` (supported internally by FTD). This will be the default color for the text

   color: $inherited.colors.text

   d. Now add the condition to color attribute with present flag as true in the if block and pass the required color when that if block gets satisfied.
   
   color if { !$present }: $inherited.colors.error.text

Your code should look like

```
-- component display:
caption title:

-- ftd.text: $display.title
color: $inherited.colors.text
color if { !$present }: $inherited.colors.error.text

-- end: display

```

2. Now to use the display component invoke it by name

Your code should look like:

Case 1: Where boolean flag is true

```
-- boolean present: true

-- display: Hello World. Excited to use FTD

```

Case 2: Where boolean flag is false

```
-- boolean present: false

-- display: Hello World. Excited to use FTD

```

Try to run both the cases mentioned in step 2.
