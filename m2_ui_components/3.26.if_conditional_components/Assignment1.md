Write a code to create component having image and display the caption for image optionally if the value is passed to the component.

Follow below instructions to write the code:

1. Create a component with name as `image` having
   a. optional string field caption with name  `title`
   b. string field with name as `src`
   c. Add column with ftd.column
   d. Inside `ftd.column` add a image with `ftd.image` and attach the src field to the image src attribute.
   To pass the `src` field value, you have to prefix with component name like `$image.src`
   e. Now comes the optional part, pass the caption title to `ftd.text` like `$image.title`
    If the title value is not present, your code will result in error, to prevent this, we will conditionally display the text component with if attribute on the component.

Your code should look like

```
-- component image:
optional caption title:
string src:

-- ftd.column:

-- ftd.image:
src: $image.src

-- ftd.text: $image.title
if: { $image.title != NULL }

-- end: ftd.column

-- end: image

```

2. Now to use the image component invoke it by name

Your code should look like:

Case 1: Where title is passed 

```
-- image: My Image
src: https://i.ytimg.com/vi/xn61hDuj2nk/maxresdefault.jpg

```

Case 2: Where title is NOT passed 

```
-- image:
src: https://i.ytimg.com/vi/xn61hDuj2nk/maxresdefault.jpg

```

Try to run both the cases mentioned in step 2.