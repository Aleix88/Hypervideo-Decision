# Hypervideo-Card
Decision plugin for [Hypervideos.js](https://github.com/Aleix88/Hypervideos)
<div>
    <img src="https://github.com/Aleix88/Hypervideo-Questionary/blob/main/decision.png?raw=true">
</div>

## Features
- Display two different options for the user.
- For story telling videos.
- Includes a time out.

## Installation
### Manual downloading
1. Download the Decision.js file.
2. Import this file in your html.

## Usage
Add this plugin to the hypervideo configuration object with the text paràmeter on config:

    const config = {
        ...

        "tags": [
          {
            ...

            "plugin": {
                "name": "Decision",
                "config": {
                    "timeout": 10,
                    "leftButton": {
                        "timestamp": "now",
                        "text": "First option"
                    },
                    "rightButton": {
                        "timestamp": "10",
                        "text": "Second option"
                    }
                }
            }

          }, 
          ...
        ]
      };

## Config parameters

| Field | Type | Description |
| ------------- | ------------- | ------------- |
| timeout | string | Time in seconds that the user has to choose an option. By default the leftButton is selected. |
| rightButton | string | RightButton configuration object. Contains two parameters: <br/> - timestamp: time in seconds where the video will seek to. If you give it a value of "now" the video will continue on the current time. <br/> - text: the text content of the button   |
| leftButton | string | The same but with the left button. |