# Editing Projects

The project editing screen consists of three main sections. The topmost one is where you can define overall project details:

* **Project Name** - give your project a name/title here
* **Author** - provide details of the project author(s)
* **Info** - a general purpose field to store more information about the project
* **Initial scene** - once you have added scenes to your project, you must specify which scene should be initially played
* **Default choice layout** - defines the default layout used for [choices](concepts.md#choices) within the project

Use the gear icon (⚙️) next to the default choice layout selector to setup up layout settings (button colours etc.) for the default layout.

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

?> TODO

### Choices

?> TODO

#### Layouts

?> TODO

### Action Events

?> TODO

## Viewing Projects

Clicking 'View' in the top menu, or 'View project' from the side menu will take you to the project viewing page where you can test out your work. Buttons are available here to Start/Reset the project and to go full screen. Double tapping the video area provides an alternate method to enter/exit full screen mode.

!> **Full Screen Mode on iPhones and iPads**<br>Please note - due to technical limitations imposed by Apple on websites on iOS devices, this function will likely not work correctly 

## Sharing Project Links

The best way for users to access and use your Video Pathway projects is via a sharing URL that you can get by clicking the 'Share View Link' in the side menu. A simple web link will be provided that can be sent out to your users - they will be taken to a viewing screen for your project.
