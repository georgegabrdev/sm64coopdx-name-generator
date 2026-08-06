# sm64coopdx-name-generator

A lightweight, web-based tool designed to format text strings for **Super Mario 64 CoopDX**. This generator automatically handles in-game hex color syntax and converts special tag shortcuts (like `<star>`) into their corresponding in-game control characters.

---

## Features

* **Hex Color Generator:** Automatically formats your input into SM64CoopDX's required syntax (`\#RRGGBB\text`).
* **Star Icon Converter:** Converts `<star>` tags into the `U+007F` (Delete control character), which renders as the star icon in-game.
* **Live Preview:** Instant output updates as you type or change colors.
* **One-Click Copy:** Easily copy your formatted text to the clipboard with visual feedback.
* **Dark Theme:** Clean and comfortable dark mode interface.

---

## How to Use

1. Open `index.html` in any web browser.
2. Select your desired text color using the color picker.
3. Type your text in the input box. Use `<star>` wherever you want a star icon to appear.
   * *Example Input:* `Welcome <star>`
   * *Generated Output:* `\#FF0000\Welcome ` (followed by character `U+007F`)
4. Click **Copy to Clipboard** and paste the result directly into SM64CoopDX!

---

## Technical Details

* **Color Formatting:** Formats text using SM64CoopDX's string color code system: `\#RRGGBB\`.
* **Control Characters:** Replaces `<star>` (case-insensitive) with `String.fromCodePoint(0x007F)` (`U+007F`), which the game engine maps to the star font asset.
* **Dependencies:** Built using vanilla JavaScript, HTML5, and CSS3—no installation or external dependencies required.

---

## License

This project is open-source and free to use for the SM64CoopDX community.
