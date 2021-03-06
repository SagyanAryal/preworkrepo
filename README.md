# Pre-work - *Memory Game*

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program. 

Submitted by: Sagyan Aryal

Time spent: 5 hours spent in total

Link to project: https://glitch.com/edit/#!/immediate-scandalous-column?path=README.md%3A47%3A0

## Required Functionality

The following **required** functionality is complete:

* [X] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
* [X] "Start" button toggles between "Start" and "Stop" when clicked. 
* [X] Game buttons each light up and play a sound when clicked. 
* [X] Computer plays back sequence of clues including sound and visual cue for each button
* [X] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess. 
* [X] User wins the game after guessing a complete pattern
* [X] User loses the game after an incorrect guess

The following **optional** features are implemented:

* [X] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
* [X] Buttons use a pitch (frequency) other than the ones in the tutorial
* [X] More than 4 functional game buttons
* [ ] Playback speeds up on each turn
* [X] Computer picks a different pattern each time the game is played
* [ ] Player only loses after 3 mistakes (instead of on the first mistake)
* [ ] Game button appearance change goes beyond color (e.g. add an image)
* [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
* [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

I added a timer where the player has to complete the game within the given time otherwise they lose.

- [ ] List anything else that you can get done to improve the app!
The converting to GIF and posting the video part was unclear and I was not sure how to do it, so I just attached the imgur links. 


## Video Walkthrough

Here's a walkthrough of implemented user stories:
![](https://i.imgur.com/rBDyjM1.gif)
![](https://i.imgur.com/BEqyoNF.gif)

## Reflection Questions
1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here. 
[YOUR ANSWER HERE]
https://www.w3schools.com/jsref/met_win_setinterval.asp for the timer
https://www.w3schools.com/css/css3_borders.asp for rounding the shapes
2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words) 

The hardest part of developing this game was definitely getting the countdown timer to work. The first challenge I faced when creating it was trying
to figure out how to make the HTML file interact with the code from the JavaScript file. Since I had to display it counting down, the webpage would
have to have an interactive label that would display the countdown. After a quick search on the internet I realized it was possible to access and change
the HTML using the ".innerHTML" property. After that, the next step was to write the actual countdown timer code. I was unsure how JS handled time, but
again after a quick search I realized I could use setInterval() which would continually call my time function until I needed it stop by then 
calling clearInterval(). At that point I had everything I needed so I wrote my timer code which was fairly straightforward, until it wasn't. I noticed
that everytime I would restart the game, the timer would go down faster than it was suppose to. I realized that when using setInterval it would continue to 
call my function regardless of if I clicked the stop button or not. After messing around with it for awhile, I was able to resolve this issue by making my
time variable global so that I could use clearInterval() in the stop method, because previously the timer would continue to go down in the backend without being stopped
or reset. All in all, there was a lot of troubleshooting and debugging that went into this timer, but now that I finished I am glad I got to learn a lot about the interaction between JS and web development.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words) 

I noticed that if you make the web browser for the game smaller that all of the contents within that page also refactors. Specifically, the shapes go from being horizontally laid out when full-sreened to 
vertically when minimized. I am curious to learn about how to make it so that the web page becomes more responsive by making the tiles smaller but keeping the horizontal layout. 

Although the site I made here was fairly basic, I am also curious on the thought process of professional websites and how they display and design their layouts to make it appealing and user-friendly as possible. 

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words) 
[YOUR ANSWER HERE]

If I had more time to work on this project I would implement a level feature. The game would start off fairly easy where you would only have to memorize a short pattern, but as you kept guessing the patterns
correctly, the level of difficulty would go up. The difficulty itself would be determined by the countdown timer and the time in-between each pattern, and the length of the pattern itself. This would be a fun feature
to implement because it would combine every other aspect of the game into one. 


## License

    Copyright [Sagyan Aryal]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
