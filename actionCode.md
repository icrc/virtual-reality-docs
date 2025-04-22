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

When any project is running in Video Pathway, it has an accompanying 'state'. This is for storing and manipulating data that you might want to use (recording which choices were made, making random choices, etc.)

Items of data are given names within the state. These are known as 'keys'. You are free to use whatever key names you like that adhere to the follow rules:

* Keys can only contain the following characters:
  * Alphanumeric characters: `a-z`, `A-Z`, `0-9`
  * Dollar and underscore symbols: `$`, `_`
* Keys cannot start with a number
* Keys may not contain spaces

#### Writing Values
Values can be written or modified in the state using the [`setStateValue`](actionReference.md#setStateValue) action:
```
// set myValue to 37
setStateValue: "myValue", 37
```

#### Reading Values
If you want to use the values stored inside state values, simply use the key name preceded by the `@` symbol:
```
// set a state value
setStateValue: "msg", "Hello!"

// display the message stored in the state key 'msg'
showMessage: @msg
```
?> **Note**: To use a value stored in the state with other text, the key name _cannot_ be inside quoted text - it must be added outside of the quotes:
```
// Greet the user by name
showMessage: "Hello " + @name
```

### Probabilistic Execution

Sometimes it might be necessary to introduce some randomness into a project - perhaps to make the outcome of a certain choice not definite. For this purpose, it is possible to execute actions probabilistically.
This is done simply by adding a probability (a number between 0 and 1) value in square brackets after the name of the action you are executing. A probability of `0` means the action definitely won't happen, and a `1` means the action will
run with 100% certainty.

An example showing how this could be used to jump to one of two scenes randomly:
```
// Initially set the next scene id
setStateValue: "nextSceneId", 2

// Set it (with a probability of 50%) to a different value
setStateValue[0.5]: "nextSceneId", 3

// Go to the chosen scene - could be scene 2, could be scene 3
gotoScene: @nextSceneId 
```
