# ESPER v2.0

ESPER is a visual synthesizer patch built for Pure Data, GEM and the Akai APC40.

Designed to create real-time, audio-reactive visuals, I use ESPER for live VJing and experimental performances! 🎛️✨

🔸 Key Features:
* User-controlled shapes, particle systems, and video effects using GEM (https://en.wikipedia.org/wiki/Graphics_Environment_for_Multimedia) 🔺💫
* Live video-feed integration for dynamic visuals (and video feedback) 🎥
* Audio-reactive components for immersive, sound-driven experiences 🎶

While there’s always room for improvement, I’m really happy with how fun and interesting ESPER has become to use—so I thought it was time to share it with you all! 🙌

Since Pure Data and GEM are free and open source, I encourage you to tweak, remix, and experiment with this patch to your heart's content. Although designed for the Akai APC40, it can be mapped for different controllers. Or even just as a reference to learn more about how GEM and Pure Data work! 🛠️✨

(When I started, my knowledge of Pure Data and GEM was practically nothing, so this has been an incredibly fun and rewarding journey for me) 

## How-To

If you dont have Pure Data already, download Pure Data vanilla here - https://puredata.info/downloads

Open Pure Data, and download the external called GEM. (In the Help tab, click 'Find Externals' and search for 'GEM'.

Download this repo.

Plug in and turn on your Akai APC40.

Launch Pure Data and make sure it is recieving messages from the APC40 (see Midi Settings)

Make sure all your APC Track Activators are set to 'Off'. 

Launch the apc-gui.pd file. This shows some helpful info about what tracks and functions are toggled on, so it is helpful to monitor during use. Usually I will have this screen up during a performance, and the GEM window open on a seperate monitor.

v1.5 also includes a stand alone gui that provides a different layout meant for performanced without the APC40. This is the standalone-gui.pd file.

Press 'Play' on your APC or in the GUI. This will start the GEM Window.

You will see the GEM window pop up with all 8 tracks enabled. I like to go through and toggle all tracks off so as to start with a blank canvas.

There are 8 'tracks' or 'layers' in ESPER. Much like you would use the APC40 for Music production, each track corresponds to one layer.

The 'Track Select' buttons on the APC allows you to toggle through the effects knobs for each track. The send knobs are for global and in some case webcam effects.

Consult this diagram for what all of the knobs and buttons do:

![esper-apc40-map](https://github.com/user-attachments/assets/894711aa-2529-4956-951f-aa5d936dcebe)

You can tweak performance for your machine by adjusting the frame rate, block size and other parameters in the gem-window.pd file. You can monitor CPU Usage from GUI.

Not all APC40 buttons are mapped to functions yet...!

Here is a screencap of the APC GUI

<img width="1440" alt="apc-gui" src="https://github.com/user-attachments/assets/633465d5-99b5-4770-b525-dcefb93496d9">

And the standalone GUI and GEM Window

<img width="1440" alt="standalone-gui" src="https://github.com/user-attachments/assets/145d3c7d-3d42-4f62-b90d-5cfdf5a09d5f">

## Tap Tempo

A BPM can be set by using the Tap Tempo on the APC. It averages the last four button presses into a BPM. The 'Tempo' can be started, stopped and reset with the nudge+, nudge- and shift buttons respectively. When the 'Tempo' is started, bangs are sent at every bar and quarter bar. These bangs then control various effects on various layers so that the visuals pulse to a set tempo. For example, on layer 1, when the Spin or Bounce toggles are on, the Sphere will 'Spin' and 'Bounce' at each bar (the tempo must be engaged).
Tempo currently controls tracks
* 1 - Sphere (bounce and spin)
* 4 - Grid (flip and spin)
* 6 - Wave (add noise)
* 7 - Image (spin and rotate)

## DSP

Digital Signal Processing (DSP) can be enabled by toggling on using the 'REC' button. When DSP is ON, the audio signal coming in to Pure Data is converted into an envelope to control effects and parameters of various layers. Typically the DSP controls for individual effects on a layer have a dedicated toggle. All of the toggles that are purple in the GUI control are DSP related effects. 
DSP currently controls tracks
* 1 - Sphere (size, scale, spin)
* 3 - Webcam (meta-image and cube)
* 7 - Image (rlp, sap, spin, size)
* 8 - (audio to image)

## Layers

#### Track 1 - Sphere

Particle layer with unlimited vertices.

#### Track 2 - Particles

Particle layer with limited vertices.

#### Track 3 - Webcam

Webcam layer. This layer takes the most CPU.

#### Track 4 - Ripple

A "grid" which can be "rippled"

#### Track 5 - Square Particles

Actually Track 9 in the code. A rotating line of squares which can be bent. An adaptation of this PD live coding video - https://www.youtube.com/watch?v=kua7TZtroY4&ab_channel=SungminPark

#### Track 6 - Wave

Creates a newWave object. Pulse it with "Noise" (pad 6-1, 6-2, 6-3, and 6-4) or a "Wave" (6-5)

#### Track 7 - Image

In the Images folder are four images (img1.jpg, img2.jpg, img3.jpg, img4.jpg). You can replace the images in this folder to load in your own images into ESPER. Just be sure that the file names stay the same and you use a .jpg extension. 

#### Track 8 - Audio to Image

Using DSP, the incoming audio signal is converted into a pixelated images

## v2 updates include:
- track 5 has been given an overhaul to be a more interesting 'spring' of rotating squares
- The standalone GUI has been given a facelift and is less busy / more readable
- A new image is loaded in the "Images" directory for Track 7 to use.
- Track 1 is given an extra DSP control for 'Spread'
- Track 4 is given an extra slider to control the ripple intensity 'Amount'
- colour changes are now synced to the tempo (if supplied)

## Trailer / Examples

https://youtu.be/dnWvNLu04hQ
https://youtu.be/nn5tZCgdM9w

<img width="1440" alt="Screen Shot 2024-10-04 at 1 27 00 PM" src="https://github.com/user-attachments/assets/a0474c5e-32dc-4532-b92e-6935b753a4b7">
<img width="1440" alt="Screen Shot 2024-10-04 at 1 26 17 PM" src="https://github.com/user-attachments/assets/492dbe7d-6472-4f9c-9ec3-b957d5b50f01">
<img width="1440" alt="Screen Shot 2024-10-04 at 1 25 39 PM" src="https://github.com/user-attachments/assets/00960118-79f9-40f7-80ed-0a751cc0e123">







