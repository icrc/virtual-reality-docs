# Action Code - Making Things Happen

Within [Choices](concepts.md#choices) and [Action Events](concepts.md#action-events) you will come across 'actions'. These allow you to make things happen within your project - jumping to other scenes,
displaying messages, manipulating data, etc. These actions are defined in a simple programming language called 'Action Code'. In the project editor it is possible to avoid writing this code directly when the actions you require are very simple ([gotoScene](#), [setNextScene](#), [gotoNextScene](#)) - but there are times when you will need to write this code directly.

?> The template projects available when creating a new project are a good place to help you understand how action code works.

## Syntax

The basic format for an action is as follows:
```
actionName: parameter [ , parameter2, parameter3... ]
```
The action name is simply the action you wish to run (a list of available actions can be found [here](actionReference.md)). The parameters are pieces of data/information that the action requires to do its work. If multiple parameters are required they should be separated by commas. Some actions require no parameters - in this case, the colon following the action name should be omitted:

```
actionWithNoParameters
```

Parameters that are text values should be surrounded by double quotes. Numbers can remain without quotes. Every individual action should be placed on a new line. You can add notes/comments in your code by starting a line with `//`:
```
// This is a note

// This action is passed some text
showMessage: "Hello World!"

// This action is passed a number
gotoScene: 3
```

!> **Important - if an individual parameter actually needs to contain a comma, that comma should be preceded by a backslash `\,` in order that it can be distinguished from a comma that separates parameters**


## Advanced Techniques

### State: Storing and Manipulating Values

?> TODO

### Probabilistic Execution

?> TODO
