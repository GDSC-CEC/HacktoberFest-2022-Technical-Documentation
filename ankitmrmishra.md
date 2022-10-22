# What is Responsiveness?
![responsive-web-square.jpg](https://cdn.hashnode.com/res/hashnode/image/upload/v1666439019644/YfCJh6fCo.jpg)
- In this growing era of technology we have different types of screens like mobile, laptops of different sizes, iPads of different sizes, and different sizes Tablets. 
- In Web Development it will be very hectic and everything will get muddled up if we start creating a different webpage for different sizes of screens.
- So we use **Responsiveness** while creating web pages so that they can adjust according to the sizes of the screens.

### Creating A Responsive web page.
- ***Setting up viewport***. <br>
   The viewport is the user's visible area of a web page.
The viewport varies with the device and will be smaller on a mobile phone than on a computer screen. <br>
You should include the following ```<meta>```
viewport element in all your web pages inside
```<head>``` tag.


```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
### Grid View For responsiveness.
- Many web pages are based on a ***grid-view***, which means that the page is divided into columns:
- A responsive ***grid-view*** often has ***12 columns***,  has a ***total width of 100%***, and will shrink and expand as you resize the browser window.
- First ensure that all HTML elements have the ***box-sizing*** property set to ***border-box***

 ```css
 *{
  box-sizing: border-box;
}
```

- However, we want to use a responsive grid-view with 12 columns, to have more control over the web page.
First we must calculate the percentage for one column: ***100% / 12 columns = 8.33%***. <br>
Then we make one class for each of the 12 columns. By this we can divide the width of a column according our use. 
### Media Queries
- It is the most important and most used method for responsiveness.
- It uses the
-  ```@media```
  rule to include a block of CSS properties only if a certain condition is true.
```css
/* If the browser window is 600px or smaller, 
 padding will become 2rem. */
@media only screen and (max-width: 600px) {
  body {
    padding: 2rem;
  }
}
```
### Other CSS properties to create a Responsive web page 
- Use these CSS properties for IMAGE responsiveness:-
```css
/* If the width property is set to a percentage and
  the height property is set to "auto",
 the image will be responsive and scale up and down:*/
img {
  width: 100%;
  height: auto;
}
```
```CSS
/*  If the max-width property is set to 100%, 
  he image will scale down if it has to, 
  but never scale up to be larger than its original size:*/
img {
  max-width: 100%;
  height: auto;
}
```





# What is Animation in Web Development?

Animation is the way to make a Web-page attractive and creative. 
- (here we will see animation with CSS and without javascript)
- Animation in CSS is nothing but jumping from one property and style to another.
- Here is a great website to know what animation is.
 - Click the link and you will go to a page that REACTS <br> [Garden eight](https://garden-eight.com/)
- #### What are the important properties of CSS animation

> ``@keyframes`` <br>
> [animation-name](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-name) <br>
> [animation-duration](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-duration) <br>
> [animation-delay](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-delay) <br>
> [animation-iteration-count](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-iteration-count) <br>
> [animation-direction](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-direction) <br>
> [animation-timing-function](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-timing-function) <br>
> [animation-fill-mode](https://developer.mozilla.org/en-US/docs/Web/CSS/animation-fill-mode) <br>
> animation
  
- **This 
```@keyframes```
 rule specifies the animation code.** <br>
> - The animation is created by gradually changing from one set of CSS styles to another.
> - During the animation, you can change the set of CSS styles many times.
> - Specify when the style change will happen in percent, or with the keywords "from" and "to", which is the same as 0% and 100%. 0% is the beginning of the animation, 100% is when the animation is complete. 
> - [More about @keyframes](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes)

- **The 
```animation-name```
 property specifies the names of one or more** ```@keyframes```
 **that describes the animation to apply to an element.**

  
> - Multiple
 ```@keyframes```
 are specified as a comma-separated list of names. 
> - If the specified name does not match any
 ```@keyframes```
 , no properties are animated.

- **The  ```animation-duration``` CSS property sets the length of time that an animation takes to complete one cycle.**

 ```css 
  /* Single animation */
animation-duration: 6s;
animation-duration: 120ms;

/* Multiple animations */
animation-duration: 1.64s, 15.22s;
animation-duration: 10s, 35s, 230ms;

/* Global values */
animation-duration: inherit;
animation-duration: initial;
animation-duration: revert;
animation-duration: revert-layer;
animation-duration: unset;

  ```



- **The  
```animation-delay```
CSS property specifies the amount of time to wait from applying the animation to an element before beginning to perform the animation. The animation can start later, immediately from its beginning, or immediately and partway through the animation.**

```css
/* Single animation */
animation-delay: 3s;
animation-delay: 0s;
animation-delay: -1500ms;

/* Multiple animations */
animation-delay: 2.1s, 480ms;

/* Global values */
animation-delay: inherit;
animation-delay: initial;
animation-delay: revert;
animation-delay: revert-layer;
animation-delay: unset;

```

- **The 
```animation-iteration-count```
 CSS property sets the number of times an animation sequence should be played before stopping.**
 ```css
 /* Keyword value */
animation-iteration-count: infinite;

/* <number> values */
animation-iteration-count: 3;
animation-iteration-count: 2.4;

/* Multiple values */
animation-iteration-count: 2, 0, infinite;

/* Global values */
animation-iteration-count: inherit;
animation-iteration-count: initial;
animation-iteration-count: revert;
animation-iteration-count: revert-layer;
animation-iteration-count: unset;

 ```

- **The ```
animation-direction``` CSS property sets whether an animation should play forward, backward, or alternate back and forth between playing the sequence forward and backward.**
```css
/* Single animation */
animation-direction: normal;
animation-direction: reverse;
animation-direction: alternate;
animation-direction: alternate-reverse;

/* Multiple animations */
animation-direction: normal, reverse;
animation-direction: alternate, reverse, normal;

/* Global values */
animation-direction: inherit;
animation-direction: initial;
animation-direction: revert;
animation-direction: revert-layer;
animation-direction: unset;

```

- **The ```
animation-timing-function``` CSS property sets how an animation progresses through the duration of each cycle.**
```css
animation-timing-function: ease;
animation-timing-function: ease-in;
animation-timing-function: ease-out;
animation-timing-function: ease-in-out;
animation-timing-function: linear;
animation-timing-function: step-start;
animation-timing-function: step-end;
```

- **The ```
animation-fill-mode``` CSS property sets how a CSS animation applies styles to its target before and after its execution.**
```css
/* Single animation */
animation-fill-mode: none;
animation-fill-mode: forwards;
animation-fill-mode: backwards;
animation-fill-mode: both;

/* Multiple animations */
animation-fill-mode: none, backwards;
animation-fill-mode: both, forwards, none;

/* Global values */
animation-fill-mode: inherit;
animation-fill-mode: initial;
animation-fill-mode: revert;
animation-fill-mode: revert-layer;
animation-fill-mode: unset;

```

- **The ```
animation``` property can be used to use all the above properties in a single property.**
```css
gdsc-cec{
animation: example 5s linear 2s infinite alternate;
}
```

 