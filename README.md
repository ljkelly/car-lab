# Car Lab

## ELE 302: Building Real Systems, Princeton, 2015

During the Spring semester of my Junior year at Princeton, I took ELE 302 and built an autonomous electric vehicle. Starting with an RC electric hobby car, [Ryan O'Shea](http://www.ryanoshea.com) and I stripped out the radio module and motor and steering controllers, then built replacements from scratch.

TL;DR: [video of the car](https://www.youtube.com/watch?v=azzE5iQZgSc) // [photos of the car](https://www.flickr.com/photos/rinoshea/albums/72157651516510906)

A photo of the final car:

![](images/final%20car.jpg)

You can find more photos [on Flickr](https://www.flickr.com/photos/rinoshea/albums/72157651516510906).

- **[Stage 1: Speed Control](https://github.com/ljkelly/car-lab/blob/master/Stage%201%20Report%20-%20Speed%20Control.pdf):** We designed and built the circuitry to make the car travel straight at 3 ft/sec to within 2% accuracy on flat ground and 10% accuracy on an incline and decline.

- **[Stage 2: Line Following](https://github.com/ljkelly/car-lab/blob/master/Stage%202%20Report%20-%20Path%20Following.pdf):** We attached a VGA camera on a laser-etched acrylic mast, aimed at the floor. Using it, we tracked a black line on a light floor and controlled the car's steering to cause it to follow the line around a track. The car with the mast, camera, and relevant circuitry is shown below:

![](images/line%20following%20car.jpg)

- **[Stage 3: Autonomous Obstacle Avoidance](https://github.com/ljkelly/car-lab/blob/master/Stage%203%20Report%20-%20Autonomous%20Obstacle%20Avoidance.pdf):** The third stage was an independent project. We chose to implement obstacle avoidance. We mounted two sonar rangefinders to a rotating platform on the top of the car to monitor the car's surroundings. Using that data, we instructed the car to drive forward and avoid obstacles in the process, navigating around them forward and backwards if necessary. The surroundings data was also broadcast over a wireless RS232 connection to a laptop. The PSoC code used to achieve this navigation can be found in [`main.c`](https://github.com/ljkelly/car-lab/blob/master/main.c). The Matlab script we wrote to parse and plot the surroundings data is [`surroundings_mapping_script.m`](https://github.com/ljkelly/car-lab/blob/master/surroundings_mapping_script.m).

**A video of the car in action can be found [here](https://www.youtube.com/watch?v=azzE5iQZgSc).**

A detail of the sonar platform is shown below, followed by an example of the surroundings data plot:

![](images/sensor%20platform.jpg)

![](images/surroundings%20plot.png)
