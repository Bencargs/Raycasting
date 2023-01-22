# Raycasting

<p align="center">
  <img src="https://user-images.githubusercontent.com/26315668/213901184-4b2475b5-e7f1-455f-a0b9-bb136c54a687.gif">
</p>

# **[Web Demo of Racasting Engine Demo][project demo]**


## Render algorithm
This engine creates a simple representation of a 3d environment, using only a 2d heightmap and some clever projection.
By tracing an arc of rays, extending from an observer against a top down image of the environment.

Each ray travels until it collides with a value on the height map, or it reaches the maximum viewing distance.

We can then determine a perspective projection rasterisation;
- We can determine what percent of our horizontal screen should be painted
  by determining what percent of out viewing arc at that distance the collision occurred,
  a collision in the middle of our viewing arc, should fill half our horizontal screen.

- We can determine the percent of vertical distance should be painted
  by determining the distance our ray had travelled, 
  a collision immediately in front of our viewer should fill the horizontal screen, 
  while it should shrink into the distance the further away it is.
  
This can be made more obvious by reducing the number of rays, and highlighting the distance of each ray:

<p align="center">
  <img src="https://user-images.githubusercontent.com/26315668/213901657-222acb0a-6dac-4998-a76f-387eaab68450.PNG">
</p>


## Links
[Web Demo of Racasting Engine][project demo]

[Raycasting intoduction](https://en.wikipedia.org/wiki/Ray_casting)

[project demo]: https://bencargs.github.io/Raycasting/
