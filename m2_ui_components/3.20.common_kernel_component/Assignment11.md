Write a code to create a container component with a text and give cursor property to the container component.

Write the code having a paragraph and cursor pointer.

Follow below instructions.

1. Create a FTD variable text with `ftd.row`

2. Add some dummy text here like below using `ftd.text`.

Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestiae, aliquid quis ea deleniti consectetur omnis harum aliquam aut nemo! Hic deserunt dignissimos cumque. Quod, nulla sit rerum labore hic ducimus.

3. Add the below attributes to `ftd.row`
width: fill-container
border-width.px: 5
border-color: $inherited.colors.text
padding.px: 10

4. Now add the cursor attribute as `cursor: pointer`

Your code should be like below:

```

-- string text: Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestiae, aliquid quis ea deleniti consectetur omnis harum aliquam aut nemo! Hic deserunt dignissimos cumque. Quod, nulla sit rerum labore hic ducimus.

-- ftd.row:
width: fill-container
border-width.px: 5
border-color: $inherited.colors.text
padding.px: 10
cursor: pointer

-- ftd.text: $text
width: fill-container

-- end: ftd.row

```

4. View your ftd file in your browser

Note: Make sure you end the row of the compnonent