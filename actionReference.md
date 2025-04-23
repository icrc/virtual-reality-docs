# Action Reference

Listed here are all the actions available within Video Pathway.

!> Actions marked with an asterisk (**\***) are **halting actions** - when these actions run, _no further actions will run after them_


## Navigation Actions


### `gotoNextScene`*

* **Purpose**: Will jump immediately to the scene current defined as the 'next' scene from the current one. The 'next' scene can be changed using [`setNextScene`](#setNextScene)

* **Parameters**: None

* **Example usage**: 

```
gotoNextScene

```


### `gotoScene`*

* **Purpose**: Will jump immediately to the scene with the specified ID. When editing action code in advanced mode, the scene ID can be looked up in the list underneath the action code editing area

* **Parameters**: Scene ID (number)

* **Example usage**: 

```
// Will jump directly to the scene with ID 3
gotoScene: 3

```


### `setNextScene`

* **Purpose**: Sets the ID of the scene that will follow when the current scene ends. Scene IDs can be looked up in the list underneath the editing area when editing actions in advanced mode

* **Parameters**: Scene ID (number)

* **Example usage**: 

```
// Sets the scene ID that will follow the current one to 7
setNextScene: 7

```


## State Manipulation Actions

### `setStateValue`

* **Purpose**: Sets the state value with the given key to the value given. The key can contain any characters from `$`, `_`, `a-z`, `A-Z`, `0-9` but must not start with a number

* **Parameters**: Key (text), Value (number or text)

* **Example usage**: 

```
// Sets the state value 'currentScore'
setStateValue: "currentScore", 0

// Sets the state value 'greeting'
setStateValue: "greeting", "Hello there!"

// Increases the state value 'currentScore' by 1
setStateValue: "currentScore", @currentScore + 1

```


### `deleteStateValue`

* **Purpose**: Deletes the state value with the given key. The key can contain any characters from `$`, `_`, `a-z`, `A-Z`, `0-9` but cannot start with a number

* **Parameters**: Key (text)

* **Example usage**: 

```
// Deletes the state value 'myValue'
deleteStateValue: "myValue"

```


## Output Related Actions

### `showMessage`

* **Purpose**: Display a popup message (message can be formatted in [Markdown](https://www.markdownguide.org/cheat-sheet/))

* **Parameters**: Message (text)

* **Example usage**: 

```
// Displays a simple message
showMessage: "Welcome!"

// Display the user's quiz score
showMessage: "You have answered " + @correctAnswers + " questions correctly"

```

?> **Note**: Video playback will pause whilst the message is displayed


### `downloadData`

* **Purpose**: Downloads the given data in CSV format. Row data should be in the form `"Value1|Value2|Value3"` 

* **Parameters**: Row data (text) - multiple rows can be specified, separated by commas

* **Example usage**: 

```
// Download a simple CSV file with the quiz results - using the first row for column headings
downloadData: 'Q1|Q2|Q3|Correct', @Q1Answer + '|' + @Q2Answer + '|' + @Q3Answer + '|' + @correctAnswers

```

