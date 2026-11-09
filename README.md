# flashcards-legacy

Keeps the old address of [Karbka](https://github.com/hlib-zinchenko/karbka), https://flashcards.hzinchenko.com/, alive after the app moved to https://app.karbka.com/.

Each person's cards live in their browser at the address they used, so the old address can't simply redirect: that would leave the cards behind and stop installed apps from updating. Instead this repository serves the same app, built with `VITE_LEGACY=1`. It works as before and shows a "Karbka has moved" screen that moves the library to the new address in one tap, or by a backup file on an iPhone home-screen app.

There is no app code here. The workflow checks out the app repository at a release tag and builds it.

## Deploy

Actions → **Deploy the old address** → Run workflow, with the app's release tag (for example `v1.0.0`). Pages: source GitHub Actions, custom domain `flashcards.hzinchenko.com`.

Keep it running for at least a year after the move: until people have moved, their cards are only here.
