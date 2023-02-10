Write a code to create component with kernel component `ftd.column` and wrap with children

Follow below instructions to write the code:

1. Create a component with name as `items` having
   a. string field value as caption `title`
   b. height and width as 50px
   c. Border width as 1px

Your code should look like

```
-- component items:
caption title:

-- ftd.text: $items.title
width.fixed.px: 50
height.fixed.px: 50
border-width.px: 1

-- end: items

```

2. Create a parent component with `ftd.column` having
   a. height and width as 200px
   b. Border width as 2px
   c. Padding as 20px
   d. Add wrap attribute as to wrap the childrens coming by `items` component

Your code should look like

```
-- ftd.column:
width.fixed.px: 200
height.fixed.px: 200
border-width.px: 2
padding.px: 20
wrap: true

-- items: 1

-- items: 2

-- items: 3

-- items: 4

-- items: 5

-- items: 6

-- end: ftd.column

```
