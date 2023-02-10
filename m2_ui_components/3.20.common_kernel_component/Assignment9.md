Write a code with a paragraph having width of 300px.

(Give background color for a great experience).

Follow below instructions.

1. Create a FTD variable text with `ftd.text`
2. Add some dummy text here like below.

Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestiae, aliquid quis ea deleniti consectetur omnis harum aliquam aut nemo! Hic deserunt dignissimos cumque. Quod, nulla sit rerum labore hic ducimus.

3. Now add the border using `border-width.px` with value as 5
   And `width.fixed.px` as `300`

Your code should be like below:

```

-- string text: Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestiae, aliquid quis ea deleniti consectetur omnis harum aliquam aut nemo! Hic deserunt dignissimos cumque. Quod, nulla sit rerum labore hic ducimus.

-- ftd.text: $text
width.fixed.px: 300
border-width.px: 5

```

4. View your ftd file in your browser

Note:

Give a try for min-width and max-width.

Sample Code:

```
-- ftd.text: $text
min-width.fixed.px: 1000
border-width.px: 5

-- ftd.text: $text
max-width.fixed.px: 1000
border-width.px: 5
```

Alternatively you can give `fill-container` as value for min-width and max-width, like below

```
-- ftd.text: $text
border-width.px: 5
min-width: fill-container

```