Write a code that gives the border to a text with width as 2px.

Follow below instructions to create a color modes text.

1. Create a FTD variable text with `ftd.text`
2. Add some dummy text here like below.

Border content with hello world

3. Now add the border using `border-width.px` with value as 5
And `border-color` as red with ftd.color 

Your code should be like below:

```

-- ftd.color red:
light: red
dark: red

-- string text: Border content with hello world

-- ftd.text: $text
border-width.px: 5
border-color: $red
```

4. View your ftd file in your browser

Note: Try out below border attributes examples to allow border colors optionally from top, right, left and bottom directions.

border-top-color: $red
border-left-color: $red
border-right-color: $red
border-bottom-color: $red
