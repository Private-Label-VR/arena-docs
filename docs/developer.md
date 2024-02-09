# Developer Commands

Welcome to the developer commands guide for controlling your Private Label VR Virtual Reality Arena! This guide will provide you with the necessary information to send commands to the arena server via UDP packets containing JSON payloads.

## Server Details

- **IP Address**: 10.55.0.10
- **UDP Port for Commands**: 53010
- **UDP Port for Responses and Events**: 53011
- **Message Type**: Unicast

## Commands

### Control LEDs

#### JSON Command Example:

```json
{
  "command": "control_leds",
  "led_color": "blue",
  "brightness": 50
}
```

#### Response:

```json
{
  "status": "success",
  "message": "LEDs controlled successfully"
}
```

### Play Music

#### JSON Command Example:

```json
{
  "command": "play_music",
  "song": "theme_song.mp3"
}
```

#### Response:

```json
{
  "status": "success",
  "message": "Music started playing"
}
```

### Set Attract Mode Settings

#### JSON Command Example:

```json
{
  "command": "set_attract_mode",
  "duration": 60,
  "video": "attract_video.mp4"
}
```

#### Response:

```json
{
  "status": "success",
  "message": "Attract mode settings updated"
}
```

### Subscribe to Events

#### JSON Command Example:

```json
{
  "command": "subscribe_events",
  "events": ["attendant_needed", "card_swipe"]
}
```

#### Response:

```json
{
  "status": "success",
  "message": "Events subscribed successfully"
}
```

## Events

### Attendant Needed

When an attendant is needed, the server will send the following event:

```json
{
  "event": "attendant_needed",
  "location": "VR Station 3"
}
```

### Card Swipe

When a card is swiped, the server will send the following event:

```json
{
  "event": "card_swipe",
  "card_number": "1234567890"
}
```

## Acknowledgement

Each command will return an acknowledgement in the form of a JSON response with a status and message field indicating the success or failure of the command execution.

If you have any questions or need further assistance with developer commands, don't hesitate to contact our support team at [support@privatelabelvr.com](mailto:support@privatelabelvr.com).

Happy coding!
