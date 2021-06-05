## Project Summary

In this project, we will learn how to use the css `transition` property. Transition gives us control of when a property value changes, so we can make those changes be gradual and animated.

## Steps

After each step, use git to add and commit the changes you have made to the project!

### Step 1.

Fork this repository to create your own copy.

### Step 2.

Make `index.html` and `style.css` files. Use HTML:5 snippet and link the style sheet to the html. We will also want to link the `reset.css` file that is included in the repo. Make sure to link `reset.css` before `style.css` so that the reset styled are applied first.

In this step, let's also go ahead and change the title for our website. You can make it whatever you want.

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Transition</title>
  </head>
  <body></body>
</html>
```

</details>

### Step 3.

Let's create 3 squares.

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Transition</title>
  </head>
  <body>
    <div class="square"></div>
    <div class="square"></div>
    <div class="square"></div>
  </body>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
.square {
  width: 200px;
  height: 200px;
  margin: 16px;
  background-color: #123456;
}
```

</details>

### Step 4.

Now let's make it so when we hover over the squares, they grow in size.

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Transition</title>
  </head>
  <body>
    <div class="square"></div>
    <div class="square"></div>
    <div class="square"></div>
  </body>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
.square {
  width: 200px;
  height: 200px;
  margin: 16px;
  background-color: #123456;
}

.square:hover {
  width: 240px;
  height: 240px;
}
```

</details>

### Step 5.

We can see that when we hover over our squares, they grow in size. This is super cool! But what if we want to control the transition of changing in size? This is where the transition property comes in handy! Let's add a transition to the squares and control how long the transition takes to change the height and the width.

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Transition</title>
  </head>
  <body>
    <div class="square"></div>
    <div class="square"></div>
    <div class="square"></div>
  </body>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
.square {
  width: 200px;
  height: 200px;
  margin: 16px;
  background-color: #123456;
  transition: width 2s, height 2s;
}

.square:hover {
  width: 240px;
  height: 240px;
}
```

</details>

### Step 5.

Pretty cool! Now let's make it so the second square changes background color when we hover over it. We want this to only apply to the second sqaure. Stop reading and think for a minute on how you will do this.

We need to add a class to the second square that the other 2 squares don't have.

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Transition</title>
  </head>
  <body>
    <div class="square"></div>
    <div class="square background-change-hover"></div>
    <div class="square"></div>
  </body>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
.square {
  width: 200px;
  height: 200px;
  margin: 16px;
  background-color: #123456;
  transition: width 2s, height 2s;
}

.square:hover {
  width: 240px;
  height: 240px;
}

.background-change-hover:hover {
  background-color: lime;
}
```

</details>

### Step 6.

Great job! Now let's take control of the transition of the second sqaures background color change. We want it to take a few seconds for it to change.

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Transition</title>
  </head>
  <body>
    <div class="square"></div>
    <div class="square background-change-hover"></div>
    <div class="square"></div>
  </body>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
.square {
  width: 200px;
  height: 200px;
  margin: 16px;
  background-color: #123456;
  transition: width 2s, height 2s;
}

.square:hover {
  width: 240px;
  height: 240px;
}

.background-change-hover {
  transition: background-color 2s;
}

.background-change-hover:hover {
  background-color: lime;
}
```

</details>

### Step 7.

Now it's time to just have fun with it. Keep on practicing and creating :)
For example, let's change the second square into a circle when we hover and while the background color is changing.

<details>
<summary>index.html</summary>

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="reset.css" />
    <link rel="stylesheet" href="style.css" />
    <title>Transition</title>
  </head>
  <body>
    <div class="square"></div>
    <div class="square background-change-hover"></div>
    <div class="square"></div>
  </body>
</html>
```

</details>

<details>
<summary>style.css</summary>

```css
.square {
  width: 200px;
  height: 200px;
  margin: 16px;
  background-color: #123456;
  transition: width 2s, height 2s;
}

.square:hover {
  width: 240px;
  height: 240px;
}

.background-change-hover {
  transition: background-color 2s, border-radius 2s;
}

.background-change-hover:hover {
  background-color: lime;
  border-radius: 50%;
}
```

</details>

## Submit project

This project was just to practice using the transition property. You are not required to turn in this assignment, but I still recommend pushing it up to your github account so you can reference it in the future.
