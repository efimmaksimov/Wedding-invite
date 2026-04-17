# Project Instructions

## Iterative Layout Development

When changing HTML or CSS in this project, use screenshot-based verification whenever the visual result matters.

Use the installed Chrome binary:

```powershell
& "C:\Program Files\Google\Chrome\Application\chrome.exe" --headless=new --disable-gpu --user-data-dir="$PWD\.chrome-profile" --screenshot="$PWD\chrome-check-430.png" --window-size=430,2600 "file:///C:/Users/User/Desktop/Wedding%20invite/index.html"
```

Then inspect the generated screenshot with `view_image`.

Preferred workflow:

1. Make the smallest focused HTML/CSS change.
2. Capture a screenshot at mobile width `430px`.
3. Inspect the screenshot, especially around the edited section and nearby section boundaries.
4. Adjust CSS and repeat until the rendered result matches the requested design.
5. Keep temporary screenshots named clearly, for example `chrome-check-430.png` or `chrome-check-430-long.png`.

Chrome may need to run outside the sandbox to write screenshots. If the sandboxed command does not create a PNG, rerun the same Chrome command with escalated permissions.

The `.chrome-profile` directory is a temporary Chrome profile used only for stable headless rendering. Do not treat it as source code.
