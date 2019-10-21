Asteroids (Part 2)
==================
Now that we have a functioning space ship, we'll add some asteroids to our game. First we'll write an asteroid class that `extends Floater`.

Suggested steps to writing an Asteroid class
-----------------------------------
1. Create a new `Asteroid.pde` file in your `AsteroidsGame` folder. One way to do this is in Sublime is to choose *New | New File* and
then choose *File | Save as* and name your file `Asteroid.pde`. 
2. Write an `Asteroid` class that `extends Floater` in your Asteroid.pde file. You will need to
write a constructor and a `move()`
2. On line 14 of `index.html` add `Asteroid.pde` to the list of files in `data-processing-sources`. The canvas tag should now look like `<canvas id="AsteroidsGame" data-processing-sources="Asteroid.pde AsteroidsGame.pde Floater.pde Spaceship.pde Stars.pde">
				</canvas>`. Now choose *File | Save*.
2. Add a `int` member variable of the `Asteroid` class. It will hold the speed of rotation for each asteroid. Make sure that this is initialized to have an equal probablility of being positive or negative. Also make sure to declare it appropriately (should it be `public` or `private`?)
3. "Override" the `move()` method of the Floater class by writing a new `move()` method in the Asteroid class that also `turn`s (rotates) each Asteroid at its own speed
4. Now add just a single asteroid to your applet. Start by just calling the Asteroid's `show()` function. Make sure you can see it and are happy with its shape before going to the next step.
5. Now add the code that moves and rotates the Asteroid   

Adding an `ArrayList`
-------------------
An array probably isn't the best way to keep track of a bunch of asteroids. Arrays have a fixed size. You can't easily add or remove asteroids from an array as they are destroyed or created. A better choice might be an `ArrayList`. The `ArrayList` class has a number of useful member methods:
- `boolean add(Object x)`
- `void add(int index, Object element)`
- `Object get(int index)`
- `Object remove(int index)`
- `Object set(int index, Object x)`
- `int size()`

Suggested steps to adding an `ArrayList` of Asteroids and finishing the project
-----------------------------------

1. Create an `ArrayList` of type `Asteroid`. You may find the [ArrayList worksheet](https://drive.google.com/file/d/0Bz2ZkT6qWPYTQjFTMjhPaGNXb1E/view?usp=sharing) and the [ArrayList slide presentation](https://docs.google.com/presentation/d/1yDXGypcooCoeUa7GD99bYooRU1vBk63lC0G2JEOdTaY/edit?usp=sharing) helpful.
2. Now we'll modify the program so that when our space ship strikes an asteroid, the asteroid is removed from the `ArrayList`. Everytime an asteroid moves find the distance between that asteroid and the ship. Use processing's [`dist()`](https://processing.org/reference/dist_.html) function to find the distance between that asteroid and the ship. If the distance is less than 20 (or whatever value is appropriate for your game) remove the asteroid from the ArrayList. Otherwise, move and rotate the asteroid normally
3. Submit the same URL for your AsteroidsGame that you submitted for the two previous assignments to Google Classroom.


 
