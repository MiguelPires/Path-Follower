# Path-Follower

The goal of this project is to implement an agent (the red cone) that is able to move to a certain point in the map without colliding with obstacles or pedestraisn (the green capsules).
The agent's movement is constraint by an actuactor. This actuator either makes the agent's movement look like a car's or a human's. You can select
the which one in the Unity editor.

[![Example image](http://img.youtube.com/vi/KpZ4TUli2FY/0.jpg)](https://youtu.be/KpZ4TUli2FY) 

As you can see in the video, the agent is able to find, smooth and follow a path without colliding with anything. It's movement is constrained
by actuators that make it behave like a car (a human could also be selected). This introduces several problems and requires custom techniques to solve
since the agent can't turn without moving and, while moving, it's maximum turning angle is limited. In the case of the car, a backing up movement
was implemented that allows the car to move backwards if you click behind it (but not to far, obviously). 
The project has several components (each presents it's specific challenges):
* **Path Finding** - what is the optimal path between the agents position and the point specified by the click?
* **Path Smoothing** - path finding returns points connected by straight lines, following those lines would result in an unrealistic behaviour.
How can improve the path's quality?
* **Actuators** - how can we restrain the agent's movement to make it look like a certain type of object (e.g., human, car, etc)? How can we 
do this in a way that doesn't make navigation impossible? How do we implement specific movements (a car backing up)?
* **Pedestrian/Obstacle Avoidance** - the path returned by the path finding will never collide with a static obstacle but the movement is constrained
by the actuators so it might not be the same. How do we avoid collisions with static obstacles? How do we avoid collisions with moving objects?
* **Optimizations** -  operations like ray casts have a computational overhead (specially when executed multiple times per frame). 
Where can we optimize our program to reduce it's load and improve FPS? 
* **Pratical Problems** - the Navigation Mesh might have tiny imperfections that make following a path difficult (this isn't a theoretical problem 
but it happened). What optimizations and simplifications can we make to overcome this problem?

## Path finding

TODO


