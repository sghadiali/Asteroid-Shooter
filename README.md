# Asteroid Shooter
Note:
This Game was developed as a part of Coursera specialization Course "C# Programming for Unity Game Development" 
 
This 2D game is all about shooting Asteroids with a Turret and scoring points. Player can move the turret with direction keys and and can rotate and shoot with other keys. The Asteroid's movement is Random and the Game ends when it hits the Turret.

What did I learn?
I learnt the basics of Unity3D game engine and its connection with Visual Studio. Familiarize myself with its Layout, engine terms like rigid body, sprites, prefabs etc. How to write scripts using Visual studios and how and where to attach them to components and exploring Unity3D code documentation.
 

There are total 6 objects initially. Main Camera, Ship, HUD, EventSystem, GameAudioSource and ScoreText, which is relatve to HUD.
MainCamera contains 2 script. GameInitializer and AsteroidSpawner.
GameInitializer Initializes Screen by calling ScreenUtils script.
AsteroidSpawner Initializes the position and direction of asteroids on all 4 sides of the screen and their Directions. It used Asteroid script to do so. Asteroid class gives a random direction and gives asteroid the sufficient force to move.
The Ship object contains the Ship Script and ScreenWrapper Script. The ScreenWrapper script checks the location of Ship object and if it moves outside the camera, it re enters the object from other side of the screen. Ship script is where the inputs, corresponding to its bullet firing, moving, rotation and collision is defined. When a player fires, Ship Script Instantiate Bullet from its prefab and calls Bullet script to give it a force and a direction and also calls AudioManager class to do its work.
The HUD object contains HUD script that keeps track of score. The ScoreText object, which is a child of HUD object, defines the canvas in which the score text is displayed.
EVentSystem is the default object. 
GameAudioSource Initializes AudioManager with the required clips.

