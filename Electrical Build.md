# Electrical Build
Here is the electrical portion of my Mars Rover! This was my first experience working with a large control board with several motor controllers, power distribution, and TTL communication. Learning how to solder, splice two wires together, and debug electrical components was a large part of the learning process during this stage of the build.
## Control Board / Soldering
![IMG_0740](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/f86272b2-a131-426a-a6c7-434e98f90be9) 
![IMG_0741](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/eab33b2b-f6c2-4b08-bda8-d314930ed512) <br>
These first two images show the difference between my first time soldering and my solder connections after some experience. Clearly, there is a big difference between the clumps of solder around the pins at the beginning compared to the cone like shapes towards the end. Some electrical issues I experienced later on were due to my poor soldering connections at the beginning, so I had to return and fix those. <br>
![IMG_0742](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/d328bcaf-5c7c-4a58-aa00-b338a8a4c5af) 
![IMG_0743](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/50c80ffd-b768-437a-ba76-cbd29c057f35)<br>
Here is some more images of the soldering I had to do on the control board in order to make solid connections with the terminal blocks and the 5V/10V regulators. <br>
![IMG_0749](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/6952e479-d50d-4ff1-8079-bb1af26da415)<br>
The 2x7A motor drivers needed to be connected to the control board, so I created a series of jumper wires that connected VIN and GND to the motor controllers, as well as supplied power and ground for the motors themselves. These motor controllers connected to the terminal blocks from above with the printed wires in the PCB. <br>
![IMG_0750](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/36553d8c-2b6f-45c9-99a4-61d1ef6cd169)<br>
Here are the motor controllers attached to the rest of the control board to finish the soldering and control board build!<br>
## Raspberry Pi / Rover Code Setup
![IMG_0753](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/b5c2c665-2dd2-41e2-aa8d-5556f4a7250d)<br>
The main computer that was used for the rover was the Raspberry Pi 3b+. I was able to install Ubuntu 20.04 onto the pi and used that as the OS for the project to configure all of the files. After setting up Ubuntu, I set up the rover code which used ROS as the base framework. After configuring everything on the Raspberry Pi, I installed it onto the main control board from above. <br>
![IMG_0752](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/f5754c7e-00f4-4472-83a1-fd11d035018f)<br>
## Motor Testing / Callibration
After completing the Mechanical build and the control board build, it was time to test the connections and see if everything worked right. As is always the case with these projects it didn't go right the first time and I had to rely on process of elimination to figure out the issue. As I mentioned above, turns out it was poor soldering connections from my beginner attemtps. After fixing that, the motors worked great. <br>
![IMG_2131](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/b8d141e3-8432-4f77-bcc0-4d48bc8af2dd)<br>
To test the motors, I connected the power, gnd, and encoder wires to the terminal blocks on the control board. Then I ran PWM testing and set the quadrature encoder values to ensure proper rotation.  <br>
![IMG_2132](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/ee9b7f94-4fce-4afa-92df-145b8520e03a)<br>
This picture shows Basicmicro Motion Studio, which was the primary software I used to test the motors due to its compatability with the motor controllers. <br>
![IMG_2133](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/212499fe-719c-400f-adc7-0005e1e8f66c)<br>
Here's another cool pic of the callibration process. I had to manually test all six drive motors and all four corner motors which turned out to be easier than I anticipatd it to be, but manually screwing in the terminal blocks wasn't very fun. <br>
## Wire Connections
In order to connect all of the motors to the control board, I needed to connect six drive motors with 6 wire connections (vcc, gnd, ENC+, ENC-, ENCA, ENCB) and 4 corner motors with 5 wire connections ( vcc, gnd, ENC+, ENC-, ENCA). That's a total of 56 wire connections for the motors alone! There were also some misellaneous communication and voltage display wires I had to connect. As I mentioned earlier I learned a variety of new skills during the electrical build, like splicing two wires together as shown below. <br>
![IMG_2151](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/e9eab7c4-1cd3-4862-976b-0f1f58bab9fa) <br>
Stripping the wires.<br>
![IMG_2153](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/1313a091-2451-4322-b090-61d7f76bf071)<br>
Wrapping the two wires around one another and adding solder to splice them together. <br>
![IMG_2154](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/c664c156-8e5a-4c2e-a99c-dc56c56e57df)<br>
Using heatshrink tubing to avoid shorts with close connecting wires. <br>
![IMG_2150](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/24d4b074-d0cd-41ab-bf9c-434db344ee47)<br>
Attaching the wires to motors and feeding them through the U-Channels of the rover with wire braid. Feeding them through the half inch holes of the body wasn't the easiest task, but I managed to get them all to the main body. <br>
![IMG_2164](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/8d13a1dc-3093-484f-b39c-859460bf82ee)<br>
![IMG_2165](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/dfaff5ba-1e6b-40a9-9466-09311f145834)<br>
![IMG_2167](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/c236ba52-cc1a-40d7-9716-ae837c8ea060)<br>
These three images show the connections of the wires from the motors to the main control board. This was by far the most difficult part of the electrical assembly. Getting the wires to screw into the terminal blocks while never having a good angle to see what was happening or to even turn the screw driver was extremely tedious and required the assistance of my dad. But, when it was finished it was that much more rewarding. However, when testing the motors after the electrical assembly I realized after some debugging that I had misplaced 6 of the wires, which caused the corner motors to move either sparatically or not at all. But, once I fixed that we were good to go. <br>
![IMG_2145](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/3285c24b-cb85-4fa4-9fb8-79b6b6de6f3a)<br>
There was some additional wiring that needed to be done on the head of the rover. I had to connect the communications cable from the control board up to the head as well as the Power JST cable from the arduino shield to the RGB matrix panel itself. <br>
![IMG_2180](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/f32fb0ca-7b51-4089-987b-4b385c92dd5a)<br>
![IMG_2168](https://github.com/Hunter-Rohovit/Rubik-s-Cube-Simulator/assets/105554281/1d5a4822-a28b-41d0-bdd1-169a213d42b5)<br>
And finally the electrical build was complete!

