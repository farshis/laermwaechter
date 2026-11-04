# Lärmwächter (Noise Guard)

A kid-friendly noise meter for the game table. A sleepy animal dozes while the table is quiet and wakes up with a sound and a funny animation when it gets too loud.

**Live app:** https://farshis.github.io/laermwaechter/

## Features

- **Five animals to swipe through:** owl, cat, bear, frog and bunny. Each has its own scene, voice and set of wake-up reactions, picked at random.
- **Three states:** asleep when it's quiet, one eye open when it gets louder, wide awake (with alarm) above the threshold. The animal stays awake for at least 10 seconds.
- **Quiet stars:** the kids earn a star for every few minutes without an alarm.
- **Parent settings behind a long press** on the gear icon: alarm threshold, minimum duration, sound on/off and volume, vibration, star interval, A-weighting, calibration, language and an alarm log.
- **11 languages:** German, English, French, Spanish, Italian, Turkish, Polish, Russian, Ukrainian, Arabic and Persian (right-to-left). The device language is used by default.
- **Phone and tablet layouts**, installable to the home screen.

## How it measures

- Microphone input via the Web Audio API, with echo cancellation, noise suppression and auto gain turned off.
- Optional A-weighting filter (three biquad stages, normalised to 0 dB at 1 kHz) and "Fast" time weighting (125 ms).
- The app ignores the microphone while it plays its own sounds, so the animal doesn't wake itself up.

Phone microphones are not calibrated sound level meters. Expect a deviation of 5–10 dB unless you calibrate against a reference meter in the settings.

## Privacy

Everything runs locally in the browser. No audio is recorded, stored or sent anywhere. Settings are kept in the browser's local storage on the device.

## Limitations

- Measuring pauses while the page is in the background or the screen is locked. Keep the screen on.
- iPhones and iPads don't support vibration in the browser.

## Files

- `index.html` – the complete app (HTML, CSS and JavaScript in one file)
- `manifest.webmanifest`, `icon-*.png`, `apple-touch-icon.png`, `favicon.png` – home-screen install
