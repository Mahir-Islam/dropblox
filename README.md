# **DROPBLOX** Optimisation Challenge



Can I make a game with as few bytes as possible? I present **DROPBLOX** (not to be confused with Dropbox or Roblox), a simple arcade-style game where you must dodge as many bricks as possible. I want to create a game that looks good, gives you a lot of choice, shareable and is fun, while also having clean, readable code. My target is to crunch it down to 10kb.



Here are the parameters for the settings (removed from index.html since it was using up about 1kb of data):



##### Player Settings

* **block\_size**: *(float)* Player object size
* **block speed**: *(float)* Player object speed
* **wall\_mode**: *(integer as Boolean \[0,1])* Whether you can loop around the canvas
* **initial\_number\_of\_lives**: *(integer)* How many lives are in each game
* **life\_regeneration\_rate**: *(integer)* How many rounds before restoring a life

##### 

##### Falling Bricks Setting

* **brick\_count**: *(integer)* Number of bricks (can't have 1.5 bricks falling down)
* **brick\_height**: *(float)* Thickness of bricks
* **gap\_size**: *(float)* Gap size between bricks
* **number\_of\_gaps**: *(integer)* How many gaps are in each round. It cannot be more than **brick\_count** (otherwise it'd be too easy).



###### Brick Velocity Speed Curve

(I guess would fall under the falling bricks settings)

* **initial\_brick\_velocity**: *(float)* Initial speed of a brick (otherwise known as **c**)
* **brick\_velocity\_linear**: *(float)* Degree 1 coefficient (**b**) of brick speed
* **brick\_velocity\_square**: *(float)* Degree 2 coefficient (**a**) of brick speed

Brick speed is calculated by ax^2 + bx + c, where x is the current score of the game. It makes each round more difficult. If you want it to remain the speed every round, set **brick\_velocity\_linear** and **brick\_velocity\_square** to 0.



##### Personalisation Settings

* **display\_name**: *(string)* Name of game settings instance
* **player\_colour**: *(hexadecimal colour value)* Colour of player object
* **brick\_colour**: *(hexadecimal colour value)* Colour of falling bricks
* **canvas\_height**: *(integer)* Height of canvas (making it too high may create formatting problems)
* **canvas\_width**: *(integer)* Width of canvas
* **canvas\_colour**: *(hexadecimal colour value)* Colour of canvas background
