# Format Server

## Start Format server
In Terminal 
```
npm start
```

## Add Story Format
In Twine, add Story Format:
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

[[Give me a quest!->appleQuest]] 
<!--showif: !questReceived:appleQuest--!> # using `!` to invert condition
```

## Action
- underneath a link, add a `actions` tag:

```
Text body here....

[[Take apple->endDialog]] 
<!--actions: receiveItem:apple--!>
```
