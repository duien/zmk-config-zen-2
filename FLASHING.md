## How to easily download firmware and flash

Push your changes to github, then use the custom flashing utility to:
- watch the build until it's done, 
- then download the resulting firmware into a directory corresponding to the SHA of the current commit,
- then move the firmware onto the board with prompts for when to connect.

When prompted, double-press the reset button to put it into flashing mode before plugging in USB.

```fish
./zen-flash
```

