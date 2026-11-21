# Tara Gala

**Tara Gala! Bawat biyahe, may kuwento.** Tara Gala is a Road Trip & Overlanding Planner for trips with long drives, island crossings, RORO ferries, campsites and hotels. *Walang iwanan, puro gala lang!*

It is a single `index.html` file: plain HTML, CSS and JavaScript, no build step and no backend. Your trips are saved on your device first, and (optionally) synced to a **private folder in your own Google Drive** so they follow you across your laptop, phone and tablet.

## Features

### Organize
- **Trip Groups** on the home screen, in grid or list view. Rename, open and delete groups safely: deleting a group with trips makes you move them first, and deletions can be undone.
- **Trips** inside each group, each with an editable title ("San Tayo?" until you name it), a breadcrumb back to its group and a CSV export.
- **Itinerary legs** with route name, date, departure time, starting point, destination, travel mode (Drive or RORO / Ferry) and arrival time, including journeys that cross midnight.
- **Smart defaults:** a new leg starts at the previous leg's destination, on its arrival date and time, with the same fuel price and km/L.

### Plan and track
- **Statuses:** planned, in progress (one at a time, highlighted) and completed (moved into a collapsible section, restorable, with undo).
- **Expenses:** fuel (distance ÷ km/L × price), food and dining, accommodation, RORO ferry and terminal, miscellaneous, with a category breakdown and totals.
- **Accommodation:** where you are staying, check-in and check-out times and the price.
- **Route itinerary as cards:** each leg is a card in one row that scrolls and snaps sideways (three cards at a time on large screens, two on tablets, one on phones), with a card navigator (first, previous, next, last and a slider) and a labeled action bar (Navigate, Live, Done, View, Delete). Phones can switch between a swipeable row and a vertical list. Cards out of view are dimmed, and the leg view fills the screen on small screens.
- **Leg notes:** a free-text note per leg, shown on the card, in the leg view and in the CSV.

### Google Maps (optional)
Place search, a map picker with search and My location, automatic distance and driving time, estimated arrival and one-tap Google Maps navigation. Without a Maps key everything can still be typed by hand.

### Login page
A welcome screen appears on your first visit: **Continue with Google** (sign in and sync right away) or **Continue with local data** (go straight to the home page, and sign in later in Settings). If you have connected a Google account before, the login page appears once per browser session as **Welcome back**, with one tap to reconnect or to carry on with the trips already on your device.

### Smooth motion
Screens cross-fade, cards and groups rise in one after another, cards slide away before they are removed while the rest glide into place, the sync banner slides open and closed, and theme changes fade. Everything shares one set of timings and easing, and it all switches off if your device is set to reduce motion.

### Saved on your device, synced to your Google Drive
- **IndexedDB** is the working database, so Tara Gala is fast, saves every change immediately and keeps working offline.
- **Google Drive sync** (optional): sign in with Google and your trips are backed up automatically while the app is open. A sync chip shows **Synced, Syncing, Pending changes, Offline, Reconnecting, Reconnect, Sync failed or Conflict**, with a **Sync now** button in Settings.
- **Conflict-safe:** if two devices change the same item, nothing is overwritten. You choose what to keep (or keep both). Changes to different items merge on their own, and deleted items stay deleted on every device.
- **Backups:** export and restore a JSON backup, export a trip as CSV, restore the cloud backup or the previous cloud backup, and undo a restore. Backups from older versions of Tara Gala can still be imported.
- **Appearance:** dark and light modes, color combinations and font options. These stay on each device.

## How sync works (and what it can't do)

1. Every edit is written to IndexedDB first. Then it is marked as pending and uploaded about two seconds later (rapid edits become one upload).
2. The cloud copy is a versioned JSON file, `tara-gala-backup.json`, in your Drive's private **appDataFolder**, plus `tara-gala-backup.previous.json` as a recoverable earlier version.
3. Before uploading, Tara Gala checks that the cloud file hasn't changed since it last looked. If it has, it downloads it and does a three-way merge against the state both sides last agreed on. Items changed on only one side merge automatically. Items changed on both sides are shown to you.
4. Opening the app on another device downloads the newest cloud data, and while the app is open it checks for changes every 90 seconds.

**Limits you should know about**
- Google's browser sign-in issues short-lived tokens (about an hour) and no refresh token. Tara Gala keeps the token in memory only, never in storage, so **after about an hour, or each time you reopen the app, tap Reconnect** to keep syncing. Your changes stay safe on the device in the meantime.
- Sync runs only while the app is open, online and connected. There is no background sync after you close the browser.
- Google Drive's API has no atomic "write only if unchanged", so Tara Gala checks the file version right before writing. If two devices write within the same fraction of a second, the later write can replace the earlier one, so one device's very latest edit may be overwritten. This is rare, and the check shrinks the window as far as the API allows. The previous cloud backup and a JSON backup are your way back to an earlier state.
- Opening Tara Gala for the first time while fully offline needs the page to be in your browser's cache. After that, your saved trips work without a connection.

## Google Cloud setup (once)

Tara Gala ships with an OAuth Client ID in the `GOOGLE_CLIENT_ID` constant near the top of the script in `index.html`. To use your own Google Cloud project:

1. Open the [Google Cloud Console](https://console.cloud.google.com/) and create (or pick) a project.
2. **Turn on the Google Drive API:** *APIs & Services → Library → Google Drive API → Enable.*
3. **Configure the OAuth consent screen:** *APIs & Services → OAuth consent screen.* Choose **External**, add your app name and email, and add the scopes `openid`, `email`, `profile` and `https://www.googleapis.com/auth/drive.appdata`. While the app is in **Testing**, only the test users you list can sign in. Add yourself and anyone else who will use it.
4. **Create the OAuth client:** *APIs & Services → Credentials → Create credentials → OAuth client ID → Web application.* Under **Authorized JavaScript origins** add the address Tara Gala runs from, for example `https://your-username.github.io` (just the origin, with no path and no trailing slash) and `http://localhost:8000` if you test locally. You do **not** need an authorized redirect URI.
5. Copy the **Client ID** (it ends in `.apps.googleusercontent.com`) into the constant:

   ```js
   const GOOGLE_CLIENT_ID = "1234567890-abc123.apps.googleusercontent.com";   // CONFIG
   ```

   The Client ID is public by design. Never put a client secret anywhere: Tara Gala doesn't use one.
6. In the app, open **Settings → Google Drive sync → Sign in with Google**.

Common errors: `origin_mismatch` means the page's address isn't listed under Authorized JavaScript origins. "Access blocked" means you aren't a test user yet. "Drive API isn't turned on" means step 2 was skipped. Google sign-in doesn't work from a `file://` page, so host the app or use `http://localhost`.

### Google Maps key (optional)
In **Settings → Google Maps**, paste an API key from a project with **Maps JavaScript API**, **Places API (New)** and **Routes API** enabled (and **Geocoding API** for addresses of pinned locations). Restrict the key to those APIs and your site's address. The key is saved only in your browser. It is never put in the code, a backup or the cloud.

## Deploying with GitHub Pages
1. Put `index.html` (and this `README.md`) in the root of your repository on `main`.
2. *Settings → Pages → Build and deployment → Deploy from a branch → `main` / `(root)`.*
3. After a minute or two the app is live at `https://<your-username>.github.io/<repository-name>/`. Add `https://<your-username>.github.io` to the OAuth client's Authorized JavaScript origins.
4. Hard refresh (Ctrl+Shift+R, or Cmd+Shift+R) after each deploy so the browser loads the new file.

## Privacy and security
- Sign-in uses Google Identity Services in the browser. Only these scopes are requested: `openid`, `email`, `profile` and `drive.appdata`. Tara Gala can't see your other Drive files.
- No client secret exists in the app. Access tokens live in memory only and are never saved in localStorage, IndexedDB or a backup.
- Your trips go only to your own device and your own Drive appDataFolder. There is no analytics, no tracking and no other server.
- Client-side code is visible to anyone, so don't treat it as access control. Your Drive data is protected by your Google account.

## Data
- Records have stable IDs, `updatedAt` times and delete tombstones: `groups`, `trips` (with a `groupId`) and `legs` (with a `tripId`).
- Backup format: `{ app, schemaVersion, appVersion, lastUpdated, groups, trips, legs, settings, syncMetadata }`, currently `schemaVersion: 2` (version 2 added per-leg notes). Version 1 backups still import, and an older copy of the app that sees a version 2 backup stops syncing and asks you to update instead of dropping your notes, so update every device together.
- Existing data from earlier versions is moved into IndexedDB automatically on first open (into a "My Trips" group). The original browser data is left in place.

## Version history

The current version is shown in the app footer and on the Settings page. Every change gets a new version: patch (x.y.1) for fixes, minor (x.1.0) for features, major for big architecture changes. Update `APP_VERSION` near the top of the script in `index.html` and add a row here.

| Version | Changes |
| --- | --- |
| 4.1.0 | Route itinerary rebuilt as a swipeable card row with a card navigator, labeled action bar, phone layout switch and floating Add trip leg button (not shown on phones). Per-leg notes. New login page with Continue with Google or Continue with local data. Screens cross-fade, lists and cards animate in and out, and the sync banner and theme changes are smooth. Backup schema version 2. Conflict review now shows the differing values. |
| 4.0.0 | Google sign-in and private Google Drive sync. Trips now live in IndexedDB and work offline. New home screen with Trip Groups, groups of trips and trips of legs. Safe three-way sync with conflict review, delete tombstones and a previous cloud backup. Versioned backups, with older JSON backups still importable. No floating Add leg button on phones, right-aligned modal footers and larger action icons. |
| 3.6.1 | On phones, the buttons in the footer of every window are aligned to the right, with the main action at the bottom right, for easier one-handed use. |
| 3.6.0 | Fuel and accommodation amounts show on itinerary cards (and under the row in the table) when entered. Quick Drive / RORO-Ferry toggle per leg. Mark a leg as in progress, with a highlighted card. Buttons adapt to small phone screens. Font options in Settings. |
| 3.5.2 | Departure times in the itinerary use the 12-hour format (for example 10:00 PM). Arrival and check-in/out times use capital AM/PM too. |
| 3.5.1 | Smoother completed-leg flow: cards slide away, the rest of the page glides into place, the Completed legs panel eases open and closed, and its rows rise in one by one. |
| 3.5.0 | Mark trip legs as complete. Completed legs move into a collapsible "Completed legs" section where they can be viewed, restored (marked as incomplete) or deleted. Undo after marking. |
| 3.4.0 | The map picker now has a place search box and a My location button, in addition to tapping or dragging the pin. |
| 3.3.0 | Smooth open and close motion for the leg view and all other dialogs. On phones and tablets the leg view slides up like a sheet, and its sections fade in one after another. |
| 3.2.1 | Removed the blue tap flash on mobile. Cards and buttons still open and respond to taps. |
| 3.2.0 | Tap or click an itinerary row or card to open the leg view. The leg view fills the screen in card view. The Add leg button floats at the bottom right while scrolling. Smooth transitions on all buttons. |
| 3.1.0 | "Estimated costs" renamed to "Expenses". Food & dining, RORO ferry & terminal and Miscellaneous amounts are shown in the itinerary (₱0 in the table, hidden on cards when empty). Cards now take over from the table at 1400 px and below, and the expenses panel sits below the itinerary. |
| 3.0.3 | The leg number is shown at the top of each itinerary card on tablets and phones. |
| 3.0.2 | Route name placeholder changed to "e.g. Manila to Baguio". |
| 3.0.1 | The "Staying at" strip is hidden in the itinerary for legs with no accommodation note. |
| 3.0.0 | Route names, read-only view mode for legs, accommodation check-in and check-out, starting point inherits the previous destination, save-or-discard prompt on the leg form, durations shown as hrs and mins, trip summary with total days, staying-at strip in the itinerary, and Settings with dark/light mode and extra color combinations. |
| 2.8.0 | Accommodation notes: record where you are staying for each leg (for example "Dencels Hotel"). Shown in the itinerary and included in the CSV export. |
| 2.7.0 | A new trip leg starts on the previous leg's arrival date and time by default. It can still be changed. |
| 2.6.1 | Roomier itinerary table: every value stays on one line except Route. Wider page, and the expenses panel sits below the table on screens narrower than 1440 px. |
| 2.6.0 | Backup and CSV file names follow the trip title. App version shown in the footer and Settings. |
| 2.5.2 | The default title "San Tayo?" shows until the user names the trip. Any name, including "Gala-nelos Overland Trip 2026", is accepted. |
| 2.5.0 | New default title "San Tayo?" with a "Your next adventure" label and a naming prompt. |
| 2.4.0 | Tara Gala browser tab icon. |
| 2.3.0 | Start trip in Google Maps from the leg form and the itinerary. |
| 2.2.0 | Tagline "Road Trip & Overlanding Planner" and an overlanding rig logo. |
| 2.1.0 | Fuel price and km/L carry over from the previous trip leg. |
| 2.0.0 | Tara Gala branding, editable trip title, Settings page, map pin picker, total distance, automatic fuel estimate, icon buttons in the itinerary. |
| 1.2.0 | Use my current location for the starting point. |
| 1.1.0 | Google Maps place suggestions, automatic travel time and estimated arrival. |
| 1.0.0 | Dark, responsive redesign and code cleanup. |
