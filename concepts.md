# Core Concepts

To make the most of Video Pathway and this documentation, it's essential to understand all of the concepts underlying the system. This page gives a detailed overview of those concepts.


## Videos

Videos are, obviously, the most important part of a project. Any number of videos can be included in a project - they only need be available online, no uploading is required. When adding a video, you will need to specify its full web address (URL) and specify the type of video it is. Video Pathway currently supports Vimeo videos and MP4 files (a standard video file format).

Example URLs:
* **Vimeo**: `https://player.vimeo.com/video/1025039220?h=1d3c27a454` 
* **MP4**: `https://www.mywebsite.com/video123.mp4`

A title can also be given to a video for ease of reference.

## Scenes

Whilst videos provide the 'raw material' for visuals within a project, scenes define what actually gets viewed. A scene uses footage from a single video and specifies:

* The timestamp in the video where the scene starts
* The end time of the scene
* A name for the scene - to assist when editing a project
* A reference number/code for the scene - to assist with planning
* The scene that should follow this scene
* Any events (see below) that should occur during the playback of this scene

## Events

To provide interactivity when scenes are being played, we need things to happen at specific times in those scenes. In Video Pathway these 'things' are known as _Events_ and come in two types: **Choices** and **Action Events**. Launch times for these events are specified as absolute timestamps in the scene's video content.

### Choices

The user will be presented with a choice where they can select an answer/action/etc. These choices come in various forms (about which more below), and form the basis of all interactivity within a project

?> TODO

### Action Events

As well as performing actions when a user makes a choice, it is also possible to perform actions at specific times in a scene. This can be useful for [internal data processing](actionReference.md#state-manipulation-actions), [displaying messages](actionReference.md#showmessage), [downloading data](actionReference.md#downloaddata), etc.

Action events contain:

* A launch time at which to run the event.
* Details of the action(s) to be carried out

## Actions

?> TODO

