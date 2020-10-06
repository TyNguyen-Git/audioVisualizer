audioVisualizer is a HTML/CSS based audio visualizer built through the usage of canvas and the Audio Context Web API.

This project was done to practice both my CSS, HTML, and general coding foundations, as well as practice on creating static websites.

The visualizer is created by using canvas and it's ability to create create graphics continuously through the usage of javascript functions.

Once the visualizer base is drawn using canvas, the audio is sent to a function named createAudio.

createAudio uses the Audio Context Web API to create an audio analyzer node. This analyzer node then connects to the main MediaElementSource node, which is then connected to a destination which in this case represents the users speakers or headphones.

In order to visualize the audio, I take the analyser node which contains the audio file. This audio files frequency data is then transcribed into an array of 8 bit unsigned integers.

Now that the audio's frequency is now represented numerically, I call the function animationLooper which continuously creates the visualizer using the given audio frequency array.
The bars that come out of the base circle are created by setting both the start and end point of the x and y axis using some minor math. This way it is possible to control the height and width of said visualized bars.

Things I learned during this project

Web based audio devices are much more harder to handle than anticipated. Understanding the Audio Context Web API and its node usage took many hours and documentation research.

Static websites are generally bad practice for future projects. Static websites cause many issues such as dynamic sizing problems, and can end up restricting the overall scope of a project.

The way I viewed issues and how to solve them were flawed. At the beginning of this project my view of errors and bugs leaned more towards the fact that the program itself is broken and not my thought process. After many hours of failed testing, I started back at the beginning with a different outlook on how to solve issues. This included further documentation research, better understanding of the tools at my disposal, and understanding that the code is doing as instructed and I am the one at fault for the errors.
