![CORS - One system. Down to the Core.](./cors-banner.jpg)

## Banner for bundle READMEs

Put this as the first line of a bundle's README:

```markdown
[![CORS - One system. Down to the Core.](https://raw.githubusercontent.com/cors-gmbh/.github/refs/heads/main/cors-banner.jpg)](https://cors.gmbh)
```

The source is in [`banner/banner.html`](banner/banner.html). To regenerate the image (2560×800):

```shell
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --hide-scrollbars \
  --allow-file-access-from-files --force-device-scale-factor=2 --window-size=1280,400 \
  --screenshot=banner.png "file://$PWD/banner/banner.html"
magick banner.png -strip -quality 90 cors-banner.jpg && rm banner.png
```
