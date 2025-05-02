# Editing Projects

The project editing screen consists of three main sections. The topmost one is where you can define overall project details:

* **Project Name** - give your project a name/title here
* **Author** - provide details of the project author(s)
* **Info** - a general purpose field to store more information about the project
* **Initial scene** - once you have added scenes to your project, you must specify which scene should be initially played
* **Default choice layout** - defines the default layout used for [choices](concepts.md#choices) within the project

Use the gear icon (⚙️) next to the default choice layout selector to setup up default layout settings (button colours etc.) for the default layout. Default choice layouts and settings may be overridden on a per-choice basis should this be required.

## Adding Video Sources

This section allows you to add the raw [video](concepts.md#videos) sources from which scenes in the project will be derived. Clicking the `+` icon in the section header will add a new video.

You should specify:

* **Title** - a memorable title for easy identification of the video
* **Type** - the type of video being added (simple MP4 video, or Vimeo video)
* **URL** - the full web address of the video file (should start with `https://` or `http://`)

?> **Vimeo Chapters**<br>
If you select 'Vimeo' as the video type, you will notice that a button labelled 'Import Chapters as Scenes' appears. Clicking this will scan the given video for chapter markers, which - if found - will be used to create corresponding scenes in your project


## Adding Scenes

The 'Scenes' section is where you will define all of the scenes making up your project. Similar to the Videos section above, the `+` is used to add a new scene. When setting up a new scene, you may define:

* **Ref.** - a reference ID for the scene. Not required, but can be useful for the planning process of complex projects
* **Title** - a memorable title for easy identification of the scene
* **Next scene** - allows you to define the scene that will follow this one when the end is reached. If the current scene is the last one, you should select '**(n/a)**'
* **Video** - select the video source from which the scene will take its content
* **Start time** - time stamp at which the scene starts in the video
* **End time** - time stamp at which the scene ends in the video (click the **⏯** icon to choose the end of the video)

## Adding Events

Each 'Scene' on the editing page will have a section titled 'Events'. This is where the events that occur in a scene can be managed. A list of events for the scene is shown - along with icons to perform actions on that event (edit, copy, and delete). Editing of new or existing events takes place in a popup window.

Every event in a scene is either a 'Choice' or an 'Action Event'. For both types of event, a launch time must be defined - this can either be a specific timestamp or the end of the current scene (selected by clicking the **⏯** icon in the 'launch time' field).

### Choices

When adding a new 'Choice' in the popup, the following should be specified:

* **Choice layout** - this defines what layout for the text and buttons is used for this choice. All standard layout options are provided, as well as a 'default' option which will use the default choice layout defined at the project level (see [above](#editing-projects))
  * Specific options for the selected layout can be defined in the layout settings popup that can be reached by clicking the gear icon (⚙️). Any layout settings left as 'default' will use the default setting from the project level.
* **Main text** - this is the text that is displayed above/next to the option buttons for the choice. It can be left blank if you require no text to be shown
* **Timed choice** - this defines whether or not the choice should have a countdown timer. This option will determine what further options for this Choice are visible:
  * **Block (non-timed) choice options**
    * **Pause delay** - this is the number of seconds the system should wait before pausing the video after displaying the choice
    * **Background** - this defines what should happen with the video behind the displayed choice - display the current frame, display a specific frame, or show a video loop
  * **Timed choice options**
    * **Time limit** - this is the time limit the user has to pick an option from the choices available
    * **Timeout action** - defines the [action(s)](concepts.md#actions) that should occur if the user fails to make a choice before the time limit expires. See '[editing actions](#editing-actions)' below

Up to four 'choice options' (buttons) can be defined for each Choice. A simple list of these is shown, along with icons to reorder and delete them. Each one should have:

* **Text** - the text to appear on the button. If you wish to add images to the buttons it is possible to use emojis 😜
* **Action** - the [action(s)](concepts.md#actions) to carry out when the user clicks the button. See '[editing actions](#editing-actions)' below

### Action Events

These are 'invisible' events that will simply carry out [actions](concepts.md#actions) at specific times within a scene. A simple [action editing field](#editing-actions) is provided to define the action(s) that will be executed.

## Viewing Projects

Clicking 'View' in the top menu, or 'View project' from the side menu will take you to the project viewing page where you can test out your work. Buttons are available here to Start/Reset the project and to go full screen. Double tapping the video area provides an alternate method to enter/exit full screen mode.

!> **Full Screen Mode on iPhones and iPads**<br>Please note - due to technical limitations imposed by Apple on websites on iOS devices, this function will likely not work correctly 

## Sharing Project Links

The best way for users to access and use your Video Pathway projects is via a sharing URL that you can get by clicking the 'Share View Link' in the side menu. A simple web link will be provided that can be sent out to your users - they will be taken to a viewing screen for your project.


## Editing Actions

There are various parts of a project that will be require 'actions' to be defined. Where these are required, you will find specialised 'action editing fields'. These will show a summary of the existing [action code](actionCode.md), along with an edit button that will show an editor popup to assist in their modification.

Simple actions (like jumping to another scene, setting the next scene) are presented in a simplified way in the editor in order to make adding them (hopefully) more efficient. However, should the details of your required action be more complex, an advanced mode is available.

For an exhaustive list of the individual actions available - please see the [Action Reference](actionReference.md).  
