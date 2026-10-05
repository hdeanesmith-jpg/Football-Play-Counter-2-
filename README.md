# Football Play Counter

A simple iPhone app (installable web app) for tracking how many plays each player gets per half, so everyone reaches the minimum (default **7 plays per half**).

## How to use it

1. **Roster tab**: add each player's jersey number and last name. If a player isn't at today's game, tap **Here** to switch them to **Out**. They then won't count toward the goal.
2. **Track tab** (during the game):
   - Before each play, tap the number of every player who is **on the sideline** (they turn gray with a red dashed border).
   - The pill at the top shows how many are on the field. It turns green when the number matches your field size (default 11).
   - When the ball is snapped, hit **SNAP**. Every player you *didn't* tap gets +1 play, and the screen resets for the next play.
   - Made a mistake? **Undo** removes the last play and brings back that play's sideline selections so you can fix them and snap again.
   - The small number in the corner of each button is that player's count for the half. The border turns green once they reach the goal.
3. **Counts tab**: shows every player's plays for the current half, with the players who need the most plays at the top. A banner appears when everyone has reached the goal. Use **Fix a count** to adjust a number by hand.
4. **Timeouts tab**: tap **+ Us timeout** or **+ Them timeout** when a timeout is called. Each card shows how many each team has used and how many are left this half (default 3 per half, changeable in Roster → Settings). It also notes which play each timeout came before. Tap **−** to take one back.
5. Use **1st / 2nd** at the top right to switch halves. Each half is counted separately.
6. **Roster → New Game** clears the play counts and timeouts and keeps your roster.

Everything is saved on the phone automatically. Closing the app or losing signal won't lose your counts.

## Putting it on your iPhone

The app has to be hosted at a web address once. GitHub Pages does this for free:

1. On GitHub, open this repo → **Settings** → **Pages**.
2. Under **Build and deployment**, set Source to **Deploy from a branch**, pick the branch (e.g. `main`) and folder `/ (root)`, then **Save**.
3. After a minute, the page shows your URL, e.g. `https://<your-username>.github.io/Football-Play-Counter-2-/`.
4. On your iPhone, open that URL in **Safari**, tap the **Share** button → **Add to Home Screen**.

It now opens full-screen from your home screen like a normal app, and it works offline at the field.

> Note: GitHub Pages on a *private* repo needs a paid GitHub plan. If your repo is private, either make it public (the app holds no personal data; the roster stays on your phone) or use another free static host such as Netlify Drop.

## Files

- `index.html`: the whole app (HTML, CSS, JavaScript)
- `sw.js`: service worker for offline use
- `manifest.webmanifest`, `icon-*.png`, `icon.svg`: home-screen app icon and settings
