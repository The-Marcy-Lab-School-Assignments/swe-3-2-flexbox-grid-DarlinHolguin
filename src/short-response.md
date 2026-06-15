# Short Response Questions

Answer the following questions in 2-4 sentences each. Be specific and use vocabulary from the lessons.

## Question 1: Flexbox Basics

What is the difference between a **flex container** and a **flex item**? How do you make an element a flex container?

**Your Answer:**
The difference between a **flex container** and a **flex item**, is that flex item is any direct child that lives inside of a flex container.

You can make an element a flex container by applying `display:flex` to it in CSS. Once you set the display to flex all children become flex items and are arranged into rows by default.

### Syntax

```HTML
<div id='flex-container'>
    <div class='flex-item'>item1</div>
    <div class='flex-item'>item2</div>
    <div class='flex-item'>item3</div>
</div>
```

In the syntax example above the div with `id='flex-container'` is the flex container, and the three divs inside it are the flex items.

## Question 2: Main Axis vs Cross Axis

In Flexbox, what is the **main axis** and what is the **cross axis**? How do `justify-content` and `align-items` work with these axes?

**Your Answer:**
In flexbox, the **main axis** is the primary direction that flex items are laid out in, which by default runs horizontally from left to right when `flex-direction` is set to `row`. The **cross axis** runs perpendicular to the main axis, so it runs vertically by default.

`justify-content` and `align-items` both align along these axes. `justify-content` adjusts alignment along the main axis, and `align-items` controls alignment along the cross axis.

## Question 3: Flexbox vs Grid

When would you use **Flexbox** vs **CSS Grid**? Give an example of a layout that would be better suited for each.

**Your Answer:**
I would use **Flexbox** for one-dimensional layouts. Flexbox is best suited for this because one-dimensional layouts are arranged in **either** a row or a column. **CSS Grid** is generally better when you need something to be in control of two-dimensions, like arranging items across both rows and columns at the same time.

An example for a good use for Flexbox would be when aligning items in a navigational bar, usually the contents in a nav bar will be aligned in a single row. For CSS Grid would be better suited for something like arranging a photo gallery where the contents need to spread out evenly across both rows and columns.

## Question 4: The `fr` Unit

What does the `fr` unit do in CSS Grid? Explain what `grid-template-columns: 1fr 2fr 1fr` would create.

**Your Answer:**
The `fr` unit stands for "fractional unit", and what it does in CSS Grid is that it divides the grid container's available space into equal fractions and distributes them to each column. `grid-template-columns: 1fr 2fr 1fr` would create three columns that are split into 4 fractions and the middle one would be twice the size of the ones beside it. If you are wondering "why split into 4 fractions but it makes 3 columns??" well it's because 1 + 2 + 1 = 4, you can visualize it like this-

There's a pizza pie with 4 slices for 3 people. Each person (column) represents one `fr` unit-

- Person 1 gets 1 slice (`1fr`)
- Person 2 gets 2 slices (`2fr`)
- Person 3 gets 1 slice (`1fr`)

## Question 5: Media Queries

What is a **media query** and why are they important for **responsive web design**? Write an example of a media query that applies styles for screens 768px and wider.

**Your Answer:**
A **media query** is a **CSS rule** that lets you apply different CSS styles on your application dependent on the size of the screen the user is currently on, that is exactly why they are important for **responsive web design**, because this is what will allow your website to look good across different devices like phones, desktops, and tablets.

An example of a media query that applies styles for screens 768px and wider (medium devices such as tablets and desktops)-

### Example

```css
@media (min-width: 768px) {
  /*This line is the rule that sets a condition that activate if the screen width is 768px or wider */
  img {
    width: 100%;
  } /*This line sets all images to take up 100% of their containers width when the condition above is true */
}
```

## Question 6: Mobile-First Design

What does **mobile-first design** mean? What are the benefits of taking a mobile-first approach versus a desktop-first approach?

**Your Answer:**
