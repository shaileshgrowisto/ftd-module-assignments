Write a code to create component having conditional components which will be displayed when you switch from dark mode to light mode and vice versa.

Follow below instructions to write the code:

1. Create a text component with text as `You switched to dark mode`. Using `ftd.dark-mode` conditionally display this component when the value `ftd.dark-mode` is true

Your code should look like

```

-- ftd.text: You switched to dark mode
if: { ftd.dark-mode }

```

2. Create a text component with text as `You switched to light mode`. Using `ftd.dark-mode` conditionally display this component when the value `ftd.dark-mode` is false

Your code should look like

```

-- ftd.text: You switched to light mode
if: { !$ftd.dark-mode }

```

Try switching your system from dark mode to light mode

Note: `ftd.dark-mode` is a FTD variable handled directly by ftd compiler which is in sync with the system display mode and gives the boolean value as true or false.