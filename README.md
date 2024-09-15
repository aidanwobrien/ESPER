# ESPER v1.0

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

Launch the gui.pd file. This shows some helpful info about what tracks and functions are toggled on, so it is helpful to monitor during use. Usually I will have this screen up during a performance, and the GEM window open on a seperate monitor.

Press 'Play' on your APC. This will start the GEM Window.

You will see the GEM window pop up with all 8 tracks enabled. I like to go through and toggle all tracks off so as to start with a blank canvas.

There are 8 'tracks' or 'layers' in ESPER. Much like you would use the APC40 for Music production, each track corresponds to one layer.

The 'Track Select' buttons on the APC allows you to toggle through the effects knobs for each track. The send knobs are for global and in some case webcam effects.

Consult this diagram for what all of the knobs and buttons do:

You can tweak performance for your machine by adjusting the frame rate and other parameters in the gem-window.pd file. You can monitor CPU Usage from GUI.

Not all APC40 buttons are mapped to functions yet...!





