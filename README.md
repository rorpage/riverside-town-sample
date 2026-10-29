# My Riverside Town

This repository builds a [Riverside Town](https://github.com/rorpage/riverside-town) Roku screensaver from one file, `town.json`.

## Make your own town

1. Click **Use this template**, then **Create a new repository**.
2. In your new repository, open `town.json`, click the pencil icon, and change it to describe your town: the buildings and their names, colors, and fonts, the animals, the cars, and your ZIP code for the weather. The [town.json reference](https://github.com/rorpage/riverside-town#townjson-reference) lists every field.
3. Click **Commit changes**. GitHub builds your town. This takes about a minute.
4. Open the **Actions** tab, click the latest run of **Build my town**, and look at the bottom of the page. There are two downloads:
   - **riverside-town-roku**: the screensaver. It downloads as `riverside-town-roku.zip`. Do not unzip it; upload it to the Roku as it is.
   - **riverside-town-previews**: pictures of your town.

If something in `town.json` is wrong, the run fails, and its log names the field and says what is wrong.

## Install it on a Roku

1. Turn on developer mode on the Roku. On the remote, press Home 3 times, Up 2 times, then Right, Left, Right, Left, Right. Follow the steps on screen and set a password.
2. In a web browser, go to `http://<roku-ip-address>`, sign in with the username `rokudev` and your password, and upload `riverside-town-roku.zip`.
3. On the Roku, go to Settings > Theme > Screensavers and choose your town.

Developer mode allows only one sideloaded channel at a time. Installing this screensaver replaces any other sideloaded channel on the same Roku.

## Business names

You can give a shop any name, including the name of a real business. Real business names can be trademarks. A town with real business names is for your own personal use. Do not sell it or publish it as a product.

## License

This template is released into the public domain under [The Unlicense](LICENSE).
