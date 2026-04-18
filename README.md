# TiltBump

A fast, minimalist browser game where you steer a ball by tilting your phone. Knock every block off the board, survive as long as you can, and chase a higher best score each run.

## How to play

- **Mobile:** lightly tilt your phone to move the ball
- **Desktop fallback:** move the mouse slowly to steer
- Knock all blocks off the board to clear the level
- Stay on the board — if the ball falls off, the run ends
- Tap or click anywhere to start, then tap or click again to restart after game over

## Features

- Motion-controlled gameplay for phones and tablets
- Desktop mouse fallback for testing and non-mobile play
- Progressive levels
- Best score saved locally in the browser
- Mute toggle
- Mobile-friendly fullscreen styling, including safe-area handling for iPhone notch and system areas
- Single-file implementation with no dependencies

## Running locally

This project is just a static HTML file.

### Option 1: open directly

Open `index.html` in a browser.

### Option 2: serve locally

Using Python:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

Serving over HTTP is recommended, especially when testing mobile browser behavior and motion permissions.

## iPhone / iPad note

On iOS, Safari may ask for permission to access motion sensors.
If prompted, allow motion access so tilt controls can work.

## Query parameter

You can preview a specific level from the URL:

```text
?preview=5
```

Valid preview levels are clamped to a supported range.

Example:

```text
http://localhost:8000/?preview=12
```

## Tech

- Plain HTML, CSS, and JavaScript
- No build step
- No framework
- No external assets required

## Development

Since everything lives in a single file, the easiest workflow is:

1. Edit `index.html`
2. Refresh the page
3. Test on both desktop and mobile

For mobile testing, using a local server and opening the page on the device usually gives the most reliable results.

## Repository structure

```text
.
└── index.html
```

## Ideas for future improvements

- Touch controls fallback
- Difficulty modes
- Sound settings panel
- Level editor
- Procedural levels
- Shareable high scores
- Installable PWA version

## License

Add a license if you want others to reuse or contribute to the project.
