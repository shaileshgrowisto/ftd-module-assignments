Write a code to create a feature of copy and paste using global event listeners.

Follow below instructions:

1. Create a function by name as `copy` having
   a. void return type
   b. mutable string argument with name `text`.
   c. string argument with name as `val`
   d. Pass the `val` variable value to `text` variable which will will sync in the mutable variable

Your code should look like

```
-- void copy(text,val):
string $text:
string val:

text = val

```

2. Now create two variables with name
   a. `string` data type having variable name as `title`
   b. optional mutable variable with name as `copied_text` and data type as `string`

3. Display the variable `title` value with `ftd.text` component.

4. Add `$on-global-key[ctrl-c]$` event to the text component with `copy` event handler having arugment as:
   a. mutable variable reference of `copied_text` to `text` argument of the `copy` event
   b. `title` in the second argument to the `value` argument of the `copy` event

Your code should look like:

```
-- string title: Mandar Zope

-- optional string $copied_text:

-- ftd.text: $title
$on-global-key[ctrl-c]$: $copy($text = $copied_text, val = $title)

```

5. Create a row to display the copied text and place the copied message with 2 text components when the `copied_text` variables contains value conditionally.

Follow below code for reference:

```
-- ftd.row:

-- ftd.text: You copied text
padding-right.px: 10
if: { $copied_text != NULL }

-- ftd.text: $copied_text
if: { $copied_text != NULL }

-- end: ftd.row

```

Once done, run this code in your browser and validate the event by pressing keyboard keys `ctrl` and `c` together
