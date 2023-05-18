## How to easily download firmware and flash

Push you changes to github, then use the following command to watch the build until it's done, then download the resulting firmware into a directory corresponding to the SHA of the current commit.

```fish
gh run watch --exit-status; and \
    gh run download -D firmware/(git rev-parse --short HEAD) -n firmware
```

After that, you can mode into that directory and use my custom flashing utility. When prompted to connect, double-press the reset button to put it into flashing mode before plugging in USB.

``` fish
cd firmware/(git rev-parse --short HEAD)
zen-flash
```

