# Add prebuilt Format

[Download the Build File](https://github.com/dionysus/twine-to-json/blob/master/dist/twine.js)

# Add Format Server

1. In Terminal

```
npm start
```

2. In Twine, add Story Format:

```
http://localhost:3000/format.js
```

---

# Twine Scripting

## Show If

- underneath a link, add a `showif` tag:

```
Text Body....

[[Can I have your apple?!->getApple]]
<!--showif: questActive:appleQuest--!>
<!--showif: questActive:appleQuest--!> // can stack multiple conditions

[[Give me a quest!->appleQuest]]
<!--showif: !questReceived:appleQuest--!> # using `!` to invert condition
```

## Action

- underneath a link, add a `actions` tag:

```
Text body here....

[[Take apple->endDialog]]
<!--actions: receiveItem:apple--!>
<!--actions: receiveItem:apple--!> // can stack multiple actions
```
