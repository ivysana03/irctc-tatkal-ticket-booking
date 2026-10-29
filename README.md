# Tatkal Ticket Booking — Chrome Extension

Tatkal is that one minute of the day when the internet collectively holds its breath.
This extension is the friend who already has their finger on the button.

It is a browser extension plus a small React control panel that automates the boring
parts of an IRCTC Tatkal booking: the endless form filling, the dropdown archaeology,
the "did the page even load?" staring contest.

> Educational / personal project. Not affiliated with, endorsed by, or secretly sponsored
> by IRCTC. See the disclaimer at the bottom.

## What it actually does

- Auto-fills the booking journey so you are not hand-typing passenger #4's age at 09:59:58
- Runs a click loop on the buttons that need clicking, quickly, in the right order
- Lets you pre-load passengers, journey details and preferences from a side panel
- Keeps everything local — your data stays in your browser, not on somebody's server
- Ships a small options page so you can tune the timing instead of editing code

## Install it

1. Grab the latest release from the Releases page of **this** repository.
   For v6.0.0 and later, download the packaged `.zip` asset.
2. Unzip it somewhere you'll remember (not your Downloads folder, be honest).
3. Open `chrome://extensions/` in Chrome.
4. Flip on **Developer mode** (top right).
5. Click **Load unpacked** and pick the unzipped folder.
6. Pin the extension so you don't lose it in the icon haystack.

Chrome will grumble about unpacked extensions. That's normal. It grumbles at everyone.

## Use it

1. Log in to IRCTC yourself. The extension does not touch your credentials.
2. Open the extension panel and fill in your journey, passengers and preferences.
3. Get to the booking page before Tatkal opens.
4. Let it click. You watch. Try not to hover over the keyboard like a nervous parent.

If something looks off, open the options page and slow the timing down. Fast is not
always better, and IRCTC's servers have opinions.

## Build from source

Requirements: Node.js and npm.

```bash
npm install
npm run build      # builds the extension and the React app
```

Other handy scripts:

```bash
npm run build:chrome   # extension only
npm run build:react    # control panel only
npm run clean          # wipe build output
```

The unpacked extension ends up in the build output folder — load that in
`chrome://extensions/` the same way described above.

## Project layout

```
chrome-extension/   content scripts, options page, manifest
react-app/          the control panel UI
scripts/            tiny build helpers (version sync, clean)
.github/            CI workflows for building and releasing
```

## Contributing

Found a bug, or a page that changed overnight and broke a selector? Open an issue.
Pull requests are welcome — keep them focused, keep the diff readable, and please
don't add tracking of any kind.

## License

MIT. Do whatever, but read the disclaimer first.

## Disclaimer

This project exists to demonstrate browser automation techniques and is provided for
**educational purposes only**. All information is offered in good faith, with no
warranty of any kind — express or implied — regarding accuracy, reliability or fitness
for a particular purpose.

Use it in line with IRCTC's terms of service. Don't use it for bulk bookings, don't use
it for reselling tickets, and don't be the reason a rule gets added. Any misuse is
entirely at your own risk, and the authors accept no liability for loss or damage
arising from use of this software.

## Privacy

- **No data collection.** Nothing is sent to any third party.
- **Local only.** Passenger and journey details live in your browser's local storage and
  never leave your device.
- **Your consent.** By using this extension you confirm you understand what it does and
  agree to use it responsibly.
