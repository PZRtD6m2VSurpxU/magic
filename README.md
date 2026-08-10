# magic

A card trick that isn't one.

It opens as a magician's deck — riffles itself, squares up, and asks you to draw
a card. The first few draws are honest playing cards. Then, on a turn you can't
predict, the card you turn over is a hand making the circle.

You looked.

## How it works

On load the app rolls a hidden number between **2 and 5**. That's the draw the
hand shows up on. Every draw before it is a real card dealt from a shuffled
stock with no repeats, so there's no tell — no timer, no pattern, nothing to
count. It's a different number of draws every time the page loads.

Once the hand lands, the deck goes dead. Nothing resets it but a refresh.

## Running it

It's one self-contained file with no dependencies, no build step and no assets.
Open [index.html](index.html) in a browser and it works — including straight
off the filesystem.

To preview it on a local server (handy for testing on your phone over wi-fi):

```bash
node .claude/serve.js
```

Then visit `http://localhost:4173`.

To get it in front of anyone else, drop `index.html` on any static host —
Netlify, Vercel, GitHub Pages, an S3 bucket. There's nothing to configure.
Note that GitHub Pages won't serve from a private repo without a paid plan.

## Notes

- Built mobile-first and portrait-first; landscape lays the deck and the drawn
  card side by side so it doesn't break.
- Silent by design. No sound, no haptics, no share prompts.
- Ranks run A and 2–10. There are no face cards, which nobody has ever noticed
  in four draws.

## Credits

The hand is adapted from
[Okay hand gesture.svg](https://commons.wikimedia.org/wiki/File:Okay_hand_gesture.svg)
by Mohamed Ibrahim (Clker), released under
[CC0 1.0](https://creativecommons.org/publicdomain/zero/1.0/) — public domain.
It's been reoriented upside down with a tilt and re-inked to match the deck.
