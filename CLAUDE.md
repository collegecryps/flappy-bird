# Flappy Bird

A simple Flappy Bird browser game. Single file: `index.html` (HTML canvas + plain JavaScript, no build step).

- **Run it:** open `index.html` in a browser (`open index.html`).
- **Look:** the player is a ping pong ball; obstacles are red solo cups (white rim faces the gap), styled after the original Flappy Bird. Background is a night-time city (starry sky, moon, buildings with lit windows).
- **Mobile-first:** made for phones. Auto play was removed on purpose; the screen fills the phone and page zoom/scroll is blocked so taps go to the game.
- **Controls:** tap anywhere to flap (a mouse click counts as a tap on computers; no keyboard controls). Scoring: 2 points per cup passed, 1 point per bounce off a cup (ceiling bounces score nothing); the ball bounces off cups and the ceiling, and the game ends on hitting the ground or being pushed off the left edge; best score saved in the browser.
- **Tuning:** gravity, flap strength, pipe gap and speed are constants near the top of the script.
- Owner is new to coding: explain changes in plain English.
- **Online:** hosted on GitHub Pages at https://collegecryps.github.io/flappy-bird/ (repo: github.com/collegecryps/flappy-bird). Pushing to `main` updates the live site.
- **Leaderboard:** online top 10 via Supabase (table `public.scores`: name 1-12 chars, score 0-10000; anyone can read/insert, no update/delete). Called with plain `fetch` to the REST API, no npm/build step. Only the publishable key lives in the page; never use a secret/service key. After a game with points, a name box asks for a name (last one remembered in the browser). Names are drawn on the canvas (never put into HTML via innerHTML). If Supabase/internet fails, the game still works and the board says "Leaderboard unavailable".
