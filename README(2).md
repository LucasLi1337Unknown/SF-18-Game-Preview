# ♟️ Lucas Stockfish Lab

A browser-based chess playground powered by Stockfish 18, featuring game review and the extremely serious **Lucas Commentary™**.

## Features

- Play against Stockfish
- Choose White or Black
- Multiple engine strength levels
- Live evaluation bar
- Legal chess moves, check, checkmate, and draws
- Move history
- PGN import and export
- Stockfish game review
- Move classifications such as Brilliant, Great, Good, Inaccuracy, Mistake, and Blunder
- Funny Lucas-style commentary
- Browser text-to-speech commentary
- Four commentary personalities:
  - Normal Lucas
  - Rage Lucas
  - Coach Lucas
  - Absolutely Unhinged Lucas™

## Files

Keep these files together in the repository root:

```text
index.html
stockfish-18-lite-single.js
stockfish-18-lite-single.wasm
README.md
```

The Stockfish JavaScript and WASM files are required for the chess engine.

## GitHub Pages

1. Upload all four files to the repository root.
2. Commit the files.
3. Open **Settings → Pages**.
4. Choose **Deploy from a branch**.
5. Select `main` and `/ (root)`.
6. Save and wait for GitHub Pages to deploy.

## How It Works

`index.html` contains the interface, chessboard, review system, and Lucas Commentary™.

Stockfish runs in a Web Worker using:

```js
new Worker("./stockfish-18-lite-single.js")
```

The Stockfish WASM file must therefore stay beside the JavaScript file.

Chess rules are handled in the browser with chess.js loaded from a CDN.

## Lucas Commentary™

Stockfish evaluates the game and the review system turns evaluation changes into useful and/or completely unnecessary commentary.

Example:

> BRO YOUR PIECES ARE APPLYING FOR NEW OWNERS 💀

Or, on a surprisingly good move:

> A responsible move? From YOU? Character development.

## Note

This is a static website. No server or database is required.

---

Built for maximum chess and minimum emotional stability. ♟️💀
