Stuff for Zombo's Amusement
===========================



## Maze generator

[See it live](http://chrismaloney.org/ZomboApp/maze.html)

A maze comprises cells and walls.  For simplicity, to get started, we'll
just do a maze from a 2d rectangular array of square cells.  Another possibility,
for example, would be an hexagonal array.

### To do

If I ever have time, here is what I'd like to do.

* Rewrite using some drawing library
    - ✗ [Fabric.js](http://fabricjs.com/).
        - Extremely slow, when I use it to instantiate all of the 200+
          walls of the maze.  I don't see any way to tell it that these are "normal"
          static, background thingies, and don't need to be full-fledged objects.
          Compare [try-fabric/maze.html]() (native) with
          [try-fabric/maze.html?use_fabric=true]().
        - Can't use fabric and native methods together:  see
          [try-fabric/native-and-fabric.html]().
    - [Paper.js](http://paperjs.org/)
    - Easel.js

* Add a sprite that takes discrete jumps from cell-to-cell, according to the
  arrow keys.  It starts at start, of course, and the goal is to get it to the
  finish.  Optionally, let it leave a breadcrumb trail.

* Allow it to be controlled by a touchscreen

* Add sound-effects:  background music and "hooray" sound when you get to the finish.

* Make the sprite movement continuous.  When it hits a wall, make a "bong" sound.

* (Maybe) If using the arrow keys, add asteroids-like physics:  when you press an
  arrow key, the sprite *accelerates* in that direction.

* Implement a score: number of seconds, plus a penalty every time you hit a wall.

* Implement invisible walls:  there are two options (implement both):
    * sighted:  the walls in the sprite's line of sight are made visible
    * blind:  only when you bump into a wall does it become visible
  The walls' visibility decays (either after they're no longer in your line of
  sight, or immediately after you bump into them) and the decay rate is variable

* Persist user data, preferences, high scores, etc.  Ruby on Rails deployed
  through [Phusion Passenger](https://www.phusionpassenger.com/), perhaps?


## Math quiz

This will be a flashcard program.  Maybe I can make it somewhat Supermemo-like.
This will definitely need data persistence.


