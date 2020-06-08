CSS Drills
The purpose of this lab is to practice your CSS fundamentals. We'll be learning how to use and
understand the position property, and how order of specificity works in CSS. Let's go!
Setup
1. Create a new project folder and connect it to a github repository. Copy the text from this
README.md file into it.
2. Create an index.html file and a styles.css file.
3. Use the ! emmet shortcut to stub out the page.
4. In the <head> , link the the CSS file to the HTML page.
Build the HTML Structure
1. In the body element, create a div with an id of "container"
2. Add 4 div elements with a class name of "boxes" and a unique id (box1, box2, boxN) inside the
container div. Each added div will be a child of the container div and a sibling to each other.
3. Create an <h2> , <p> , and <a> element inside of each of the 4 div's. Add the following content to
the elements:
h2: Add a story title in each header
p: Add a story description within each paragraph
a: Add a link that says "Read More"
Now, Lets style!
Text and Body Styling
1. Assign a global font family
Here is a list of some Web Safe Fonts:
https://www.w3schools.com/cssref/css_websafe_fonts.asp
You could also play around with Google Fonts: https://fonts.google.com/
Hint: use the body selector.
2. Change the background color for the body element to a light grey color.
https://gravity.covalence.io/portal/course/2/43[6/12/2019 11:56:57 PM]Portal | Gravity
3. Use a multiple selector rule set to center the text for all h2 , p , and a elements.
4. Use an element selector to remove the default underline styles for anchor tags and change the
font color:
When you refresh your browser you'll notice that the link is not centered like the h2 and p
elements. This is because text-align will center the element based on the width assigned to
it. If you apply a border to the link tag, you'll see that the link is centered inside the anchor
element. The best way to center the link, relative to its parent element, is to enclose it
inside of a div element.
5. Wrap the anchor element inside of a div and give the div a class name of "readme-wrapper"
6. Replace the a in the multiple selector rule with .readme-wrapper
7. Now refresh and you'll see the link is centered as we expected it
8. Add a CSS :hover selector so that when the link is moused over the cursor changes to a
pointer, the font is bold, and text color changes.
9. Wrap a single word in each paragraph element inside of a span element and assign it a new font
color and font weight.
Box Styling
1. Use a class selector to target the .boxes class:
add margin
add padding
add a solid border with a custom color
add a border radius to round the edges of the border
add a width of 30em
2. Use an id selector to add a unique background color to each div.
Your lab at this point should resemble something like this, with the colors and margin/padding sizes
being different for you, of course! Boxes before being re-positioned
Position, how does it work?!
1. Change the display to inline-block in your boxes class selector.
Notice how the .boxes divs will now sit next to each other because of this rule.
inline-block will make block level elements flow next to each other based on their size,
instead of taking up the entire block!
2. Change the display to block in your boxes class selector.
Notice how it goes back to the previous flow without any display change? That's because
by default div elements follow block rules by default! Cool.
We're gonna leave it on block for now to do the next steps ..
3. Change the position of the second box div to be relative to its parent.
Changing that didn't seem to do anything to the flow of the page, right?
4. Now position the second box div to be to the right of the first.
https://gravity.covalence.io/portal/course/2/43[6/12/2019 11:56:57 PM]Portal | Gravity
5.
6.
7.
8.
9.
10.
11.
12.
Hint: try using bottom and left properties on the second box div with various values.
We're "nudging" this div from where it should be in the flow of elements
It won't be perfect, but it should resemble something like this, and take notice that the
element flow acts as if that div is still in its original spot!
We've moved this element relative to where it's supposed to be, without breaking the
original flow of html elements
Now change the second box div to position absolute
Madness!! Notice how it moved somewhere strange, and now the other box divs act as if
the second one isn't in the flow anymore
Adjust your position using any of the top , bottom , left , right properties to get it back to being
next to the first div.
It should look something like this, and notice that the other divs flow as if the "absolute" div
isn't included anymore!
Remove the position styling (including all the top/bottom/left/right) from the second box div.
This should make it return to what it looked like before being re-positioned.
Add a new new div element in your HTML above the h2 elements in each box. These will not
wrap anything, but rather be stand alone, i.e. <div></div> .
These divs will be representing "images" for each box
Give all four of these divs a custom class name they all share.
Select that class in your CSS, and add the following properties:
add a height and width property with a value of 50px
add a border radius property of 50px
add a custom background color
You should have something close to this with those divs added and styled, with your own color,
of course!
Use your new knowledge of positioning to get that circle next to the h2 element! Shoot for a goal
looking similar to this screenshot.
It probably won't be perfect and it might scale strangely if you change your browser size,
but that's okay! Raw CSS is tricky. We'll learn better ways to handle these issues later. :)
Styling Specificity
The following HTML code will be below the .container div, but still within your </body> . So under all
the box business you've been coding so far.
1. Below the boxes, insert 3 h1 tags into the html document, give each text for your favorite TV
shows.
2. Apply styling so that all h1’s have a font color of your choice.
3. Add 2 more h1’s with 2 other TV shows. What immediately happens to their font color when you
refresh the html doc?
4. Give all the original 3 h1’s the class name "original"
https://gravity.covalence.io/portal/course/2/43[6/12/2019 11:56:57 PM]Portal | Gravity
5. Give the additional 2 h1’s the class name "additional"
6. Apply styling by class name, have the first 3 h1’s get a new font color (don’t delete or comment
out the original styling). Once you apply a new font color by class, refresh the page and see what
it does.
7. Do the same thing for the additional 2 h1’s, give them a different font color by class name.
8. Take note at what which font color rule is in effect. Class is more specific than element in CSS
selectors! So it'll override the element selector styling and use the class selector styling.
9. Rank each TV show you have (so all 5 h1’s), a rank of show1 would be the best. Have the rank be
the id of each h1. At this point every h1 should have a class AND an id attribute.
10. Apply styling using the id of each h1, give each a different color. Refresh the document and see
how this type of styling changes what was already applied.
11. Take note that your class selectors are now overridden by the id selectors! They are more
specific and will use those styles instead of the class or element selectors on these h1's.
12. Below the h1's, create 3 unordered lists, each with 5 items, have the first list be 5 friend's names,
have the next be 5 places you want to travel, and have the last list be your favorite restaurants.
13. Apply styling to all the unordered lists using an element selector changing their font color.
14. Add the class "star" to the second and third unordered list.
15. Apply styling to the class "star" changing the font color.
16. Add the id "wars" to the third unordered list.
17. Apply styling to the id "wars" changing the font color.
18. Take note again on the order of specificity between element, class, and id selectors. element
selector styling < class selector < id selector .
19. Wrap each list in a div, give the div a border that is 2 pixels thick, have it be solid and the color be
black.
It'll look like a multi color fiasco, but the purpose here was to learn how specificity works!
But isn't styling fun? We know it can be tricky and tedious, but the more you practice, the better you'll
get at it. After a while, you won't even think about it anymore :)
Discussion
 NEW QUESTION

Confusion
https://gravity.covalence.io/portal/course/2/43[6/12/2019 11:56:57 PM]Portal | Gravity
 index.html
 GitHub
 Which README file is being referred to?
 Adding image div creates increased upper padding on parent div?
Dustin Parker
Sep 6, 2018 8:25 pm
Why does adding the div that represents the image (#21 in the first section) increase the padding
between the title and the border above it? Here is my code for the Title's div and the CSS
<div class="boxes" id="box2">
<div class="image-header"></div>
<h2>Title 2</h2>
<p>Description of <span class="color-change"> second </span> title.</p>
<div class="readme-wrapper">
<a>Read more...</a>
</div>
/* Why does adding an image increase distance from title to top border of div?*/
.image-header {
width: 1.9em;
height: 1.9em;
background-color: white;
position: relative;
top: 3.1em;
}
I had to insert the "top: 3.1em" so that it would line up correctly with the Title.
 0
 0
 RESPOND
William Johnston
https://gravity.covalence.io/portal/course/2/43[6/12/2019 11:56:57 PM]Portal | Gravity
Sep 7, 2018 5:49 pm
The h2 element comes with it's own set of default styles including some margin, so it
is probably affecting the position of other elements when you put the image div in
there.
 0
 0
 RESPOND
https://gravity.covalence.io/portal/course/2/43[6/12/2019 11:56:57 PM]