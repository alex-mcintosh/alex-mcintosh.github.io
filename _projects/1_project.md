---
layout: page
title: project 1
description: with background image
img: assets/img/12.jpg
importance: 1
category: work
related_publications: true
---

## Introduction

This is an implementation of Conway’s Game of Life using R and Plotly.
This was an exercise in using R, Plotly and Shiny for implementing the
Game of Life. The implementation of the game can be found at:
<https://xcstat99.shinyapps.io/Game_of_Life/>

## Background

The Game of Life, also known simply as Life, is a cellular automaton
devised by the British mathematician John Horton Conway in 1970. It is a
zero-player game, meaning that its evolution is determined by its
initial state, requiring no further input. One interacts with the Game
of Life by creating an initial configuration and observing how it
evolves. It is Turing complete and can simulate a universal constructor
or any other Turing machine.

This description is sourced from Wikipedia and more information can be
found here: <https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life>

## Control

Using the side panel (highlighted in red below) the size of the
‘habitat’ and the number of generations can be adjusted.
Also adjustable is the ‘Probability of starting life’, this corresponds
to p in the binomial distribution which is used for randomly assigning
the starting state.


<figure>
<img
src="https://github.com/XCStat99/Game-of-Life/assets/120208086/15c5bb52-8251-4d48-a1a1-8dee3192a6ec">
</figure>

It is also possible to adjust the rules of the Game of Life by adjusting
the text entry boxes, the default values being set to the original of
Conway’s Game of Life:

      *1. Any live cell with fewer than two live neighbours dies, as if
by underpopulation.*

      *2. Any live cell with two or three live neighbours lives on to
the next generation.*

      *3. Any live cell with more than three live neighbours dies, as if
by overpopulation.*

      *4. Any dead cell with exactly three live neighbours becomes a
live cell, as if by reproduction.*

Adjusting these leads to interesting scenarios and helps to explain why
the rules in Conway’s Game of Life described above were chosen. Once the
parameters in the control panel have been selected the simulation can be
run by pressing the ‘Start’ button.

Once ‘Start’ is pressed all generations will be calculated
and then displayed in the Plotly plot (highlighted in red below). This
may take some time for large habitats over a large number of
generations. This does lead to some limitations in performance as
outlined in the Performance Considerations section below.

    ---
    layout: page
    title: project
    description: a project with a background image
    img: /assets/img/12.jpg
    ---


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images, even citations {% cite einstein1950meaning %}.
Say you wanted to write a bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}
