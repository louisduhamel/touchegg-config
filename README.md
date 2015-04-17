# Touchegg Configuration File for Elementary OS Luna

This repository contains my Touchegg config file for Elementary OS Luna. The file was first made available [here](http://louisduhamel.fr/multitouch-os-x-like-gestures-in-elementary-os/) along with installation instructions.

The config file contains gestures for:
  - *Exposing all windows*: 4-finger swipe down
  - *Show all workspaces*: 4-finger swipe up
  - *Switching workspaces*: 4-finger swipe (left or right)
  - *Maximizing / Minimizing window*: 3-finger swipe (up or down)
  - *Tiling windows left or right*: 3-finger swipe (left or right)
  - There is also support for OS X-like "natural scrolling" and basic pinch-to-zoom.

## Using the configuration file
If you have Touchegg installed on your laptop, installing the file is as simple of copying it to  `` ~/.config/touchegg/touchegg.conf `` on your system. However, when I first tried installing touchegg using ``apt-get``, it would not work.

If the touchegg version coming from aptitude is not playing ball with your system, I suggest building touchegg from source. Here's how I did it on my machine, taking cues from [this tutorial](http://ineed.coffee/1068/os-x-like-multitouch-gestures-for-macbook-pro-running-ubuntu-12-10/) (as always, there is no guarantee that it will work on yours):

  - Download the touchégg source code from here and unpack it;
  - Download and install dependencies with this handy command: `` sudo apt-get build-dep touchegg ``. This will pull and install necessary dependencies.
  - ``cd`` to the source directory and run these commands:

  ``$ qmake``

  ``$ make``  (Note that the make command take a couple of minutes to complete; it’s okay, just look for potential errors in the output. You should be fine.)
  
  ``$ sudo make install``
  - Download the ``touchegg.conf`` file and save it under ``~/.config/touchegg/touchegg.conf``
  - Add touchegg to the list of startup applications, so that it, well, starts up at login.
  - Voila! You should be good to go.

## TODO

- This file worked fine for me on Elementary OS Luna (0.2). I'll give it a spin under Freya to see how it works.

## Questions? Comments?

If you have any questions or comments, I'd be happy to hear them! Of course feel free to fork and submit PRs. Happy hacking!

Thanks to Daniel Graziotin for his cool tutorial (available on [ineed.coffee](http://ineed.coffee)).
