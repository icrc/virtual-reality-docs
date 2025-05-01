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

The user will be presented with a choice where they can select an answer/action/etc. These choices come in two forms (block, timed) and form the basis of all interactivity within a project.

A choice has some accompanying text (a question, description etc.) and from 1 to 4 options to choose between (admittedly, a single option is not much of a choice - but there may be situations where this makes sense). Each selectable option can have an [action](concepts.md#actions) associated with it, that will be carried out when the user clicks the corresponding button.

Every choice has a layout associated with it that determines the placement and style of the displayed buttons. This layout can either be the project default, or a custom one for each choice (perhaps to best suit the current displayed video or frame).

#### Block Choices

With this type, the video will be paused until the choice is made. Whilst paused, it is possible to display:

* The current frame of the video
* A specific frame of the video
* A repeating loop of the current

Also, if required, it is possible to delay the pausing of the video until after the choice is displayed.

#### Timed Choices

This type of choice is well suited for quizzes, or 'live' situations in the video that require immediate decisions. A time limit in seconds be specified along with an optional 'timeout' action that will occur should the user not select any of the options within the time limit. The video will continue to play whilst the choice is displayed. A timer indicator will also be displayed. 

### Action Events

As well as performing actions when a user makes a choice, it is also possible to perform actions at specific times in a scene. This can be useful for [internal data processing](actionReference.md#state-manipulation-actions), [displaying messages](actionReference.md#showmessage), [downloading data](actionReference.md#downloaddata), etc.

Action events contain:

* A launch time at which to run the event.
* Details of the action(s) to be carried out

## Actions

'Actions' can occur when a user selects an option from a Choice (or perhaps doesn't select one - in the case of a Timed choice), or an 'Action Event' triggers at its specified time. They can be used to:

* [Control the flow of the video](actionReference.md#navigation-actions) (jumping directly to scenes, setting what scene comes next)
* [Perform some kind of output](actionReference.md#output-related-actions) (show a message, download data etc.)
* [Manipulate internal](actionReference.md#state-manipulation-actions) data (state)

A very simple programming language (known as '[Action Code](actionCode.md)') is used to define actions, but for simple flow control actions a simplified process is provided to set them up quickly.

