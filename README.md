# Tara Gala

**Tara Gala** is your Road Trip & Overlanding Planner para sa mga mahilig bumiyahe, mag-explore, at mag-overland — including routes na may RORO ferry crossings!

Add each drive or ferry crossing as a trip leg, and let the app calculate your distance, travel time, estimated arrival, and trip expenses. Less hassle sa planning, more time sa adventure!

It's a simple, single-file `index.html` app. No build step, no backend, and no account needed. Your trip data stays in your browser.

## Features

### Trip planning

- **Trip legs:** I-log ang bawat drive, ferry crossing, or major transfer. Add a route name, date, departure time, starting point, and destination.
- **Route names:** Give each leg a highlighted label (e.g. "Manila to Baguio") na makikita sa itinerary.
- **Editable trip title:** Name your adventure right from the page header. New trips start with "San Tayo?" and a prompt to give your gala a name. Mawawala ang prompt once you rename it.
- **Smart defaults:** Ang starting point ng bagong leg ay automatic na previous leg's destination. It also inherits the previous leg's arrival date and time. Editable pa rin lahat!
- **No lost work:** Kapag nag-click ka outside the leg form or pinindot ang Esc, the app asks whether to save or discard your changes.
- **Route itinerary:** Automatically sorted by date and departure time. Makikita mo ang distance, duration, estimated arrival, and cost for each leg. May accommodation details din, including check-in and check-out times, kapag may inilagay kang accommodation note.
- **Easy leg viewing:** Click an itinerary row, tap a card, or use the eye icon to view all leg details without accidentally changing anything. Choose Edit when you're ready to make changes. On phones and tablets, the leg view takes over the screen for easier viewing.
- **Floating Add leg button:** No need to scroll all the way back up! The Add leg button stays floating at the bottom right while you browse your itinerary.
- **Trip summary line:** See your travel dates, total days, and number of planned legs right in the header. Example: "Dec 14 to Dec 19, 2026 (6 days) • 6 legs planned".
- **Trip summary:** Check your total expenses, distance, travel time, and number of legs at a glance.

### Google Maps integration

- **Place suggestions:** Search for your starting point and destination using autocomplete, limited to the Philippines by default.
- **Pick on map:** Drop or drag a pin on a dark map instead of typing a place name.
- **Use my location:** Set your starting point using your device's current location.
- **Automatic distance and travel time:** Automatically calculate distance in kilometers and estimated driving time based on your selected places. You can still edit both manually.
- **Estimated arrival:** Calculate arrival time using the departure date, time, and travel duration — even kapag tatawid ng midnight ang biyahe.
- **Start trip in Google Maps:** Open your route in Google Maps with one click, either from the leg form or itinerary. On your phone, it can launch turn-by-turn navigation.

### Expenses

- **Automatic fuel estimate:** Calculate fuel costs using this formula:

  `Distance ÷ Vehicle consumption (km/L) × Fuel price (₱ per liter)`

- **Inherited fuel values:** Fuel price and vehicle consumption carry over from the previous leg unless you change them.
- **Expense categories:** Track fuel, food and dining, accommodation, RORO ferry and terminal fees, and miscellaneous expenses.
- **Accommodation:** Add where you're staying — campsite, hotel, or resort — together with check-in and check-out times and the accommodation price.
- **Expense breakdown:** See how much each category contributes to your overall trip budget. Bantay gastos habang gala!

### Data and settings

- **Settings page:** Manage your trip data and Google Maps connection in one place.
- **Export to CSV:** Download your itinerary and expenses for spreadsheets and further analysis.
- **Backup and restore:** Save your entire trip as a JSON file named after your trip title (e.g. `Gala-nelos-Overland-Trip-2026-backup.json`). You can restore it on another device or browser.
- **Local storage:** Your trip data is saved in your browser. Nothing gets uploaded to an external server.

### Design

- **Dark and light modes:** A low-glare dark interface by default, with a light mode available in Settings.
- **Color combinations:** Choose from five additional color combinations in each mode, or reset to the default colors.
- **Responsive layout:** Designed for desktop, tablet, and mobile. On phones, the itinerary switches to cards and forms open as bottom sheets.
- **Smooth interactions:** Buttons feature smooth transitions for a more polished experience across the app.

## Getting started

Tara, let's plan your next adventure!

1. Open `index.html` in your browser, or host the repository using GitHub Pages (instructions below).
2. Click **Add trip leg** and fill in your route details.
3. Optional: Set up Google Maps integration to use place suggestions, map pins, and automatic distance calculations.

**No Google Maps API key? No problem!** The app still works. You can manually enter places, distance, and travel time.

## Setting up Google Maps

Google Maps integration requires an API key for place suggestions, map pins, current-location names, and automatic distance calculations.

### 1. Create an API key

1. Open [Google Cloud Console](https://console.cloud.google.com/).
2. Create a project or select an existing one.
3. Create an API key under APIs & Services → Credentials.

### 2. Enable the required APIs

Enable these APIs for your Google Cloud project:

- Maps JavaScript API
- Places API (New)
- Routes API
- Geocoding API (optional — helps display pinned and current locations as addresses)

### 3. Restrict your API key

For security, configure the API key restrictions before using it publicly.

**Application restrictions:**

- Select **Websites**.
- Add your GitHub Pages address, for example: `https://your-username.github.io/*`.
- If you're using a custom domain, add that domain too.
- If testing locally through a local server, add the appropriate localhost referrer.

**API restrictions:**

- Select **Restrict key**.
- Allow only the Google Maps APIs that your app actually uses.

Also consider monitoring API usage, setting available quotas, and configuring billing alerts.

### 4. Connect the key to Tara Gala

1. Open the app.
2. Go to **Settings → Google Maps**.
3. Paste your API key.
4. Click **Save key**.

The key is stored in your browser and is not written into the app's source code or repository.

**Important security note:** A browser-based Google Maps API key is visible to visitors who inspect the website or its network requests. Storing it in browser storage does not make it secret. Website and API restrictions are essential when publishing the app. Never use an unrestricted API key in a public repository or website.

Website-restricted keys generally won't work when you open `index.html` directly from your computer using a `file://` address. Use GitHub Pages or a local development server instead.

Google Maps services may incur charges depending on usage. Check Google's current pricing, free usage limits, and billing requirements before enabling the integration.

## Deploying with GitHub Pages

Want to access Tara Gala anywhere? You can host it for free using GitHub Pages.

### 1. Create a GitHub repository

Create a new repository and upload `index.html` to its root directory.

### 2. Enable GitHub Pages

1. Open your repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose the `main` branch and `/ (root)` folder.
5. Click **Save**.

### 3. Open your app

After GitHub Pages finishes deploying, your app will be available at:

`https://<your-username>.github.io/<repository-name>/`

That's it! Tara Gala is now online. Tara na!

## Things to know

- **RORO travel time:** Google's driving estimates may not include ferry crossings, terminal waiting time, boarding, or rest stops. Add these manually to your travel duration for a more realistic arrival estimate.
- **Browser storage:** Trip data is stored in your browser's local storage. Clearing browser or website data can delete your trips, so use **Save backup** regularly.
- **Location access:** Browsers generally require a secure HTTPS connection to share your current location. The feature works on GitHub Pages but may not work when opening the app directly from a local file.
- **Google Maps billing:** Google Maps services may be subject to usage-based billing. Check the current pricing and free usage limits for your account.
- **API key security:** Browser-based API keys are visible to website visitors. Always apply website and API restrictions before publishing your app.

## Tech

Built using plain HTML, CSS, and JavaScript in a single `index.html` file.

Google Maps JavaScript API libraries used when an API key is provided:

- Maps JavaScript API
- Places API
- Routes API
- Geocoding API

No build tools, backend, or database required.

## Version history

The current app version is displayed in the footer and on the Settings page.

| Version | Changes |
|---|---|
| **3.2.0** | Itinerary rows and cards can be clicked or tapped to open the leg view. The leg view fills the screen in card view. The Add leg button floats at the bottom right while scrolling. Smooth transitions added to all buttons. |
| **3.1.0** | "Estimated costs" renamed to "Expenses". Food & dining, RORO ferry & terminal, and Miscellaneous amounts are shown in the itinerary (₱0 in the table, hidden on cards when empty). Cards replace the table at 1400 px and below, and the expenses panel sits below the itinerary. |
| **3.0.3** | The leg number is shown at the top of each itinerary card on tablets and phones. |
| **3.0.2** | Route name placeholder changed to "e.g. Manila to Baguio". |
| **3.0.1** | The "Staying at" strip is hidden in the itinerary for legs with no accommodation note. |
| **3.0.0** | Route names, read-only view mode for legs, accommodation check-in and check-out, starting point inherits the previous destination, save-or-discard prompt on the leg form, durations shown as hrs and mins, trip summary with total days, staying-at strip in the itinerary, and Settings with dark/light mode and extra color combinations. |
| **2.8.0** | Accommodation notes: record where you are staying for each leg (for example "Dencels Hotel"). Shown in the itinerary and included in the CSV export. |
| **2.7.0** | A new trip leg starts on the previous leg's arrival date and time by default. It can still be changed. |
| **2.6.1** | Roomier itinerary table: every value stays on one line except Route. Wider page, and the expenses panel sits below the table on screens narrower than 1440 px. |
| **2.6.0** | Backup and CSV file names follow the trip title. App version shown in the footer and Settings. |
| **2.5.2** | The default title "San Tayo?" shows until the user names the trip. Any name, including "Gala-nelos Overland Trip 2026", is accepted. |
| **2.5.0** | New default title "San Tayo?" with a "Your next adventure" label and a naming prompt. |
| **2.4.0** | Tara Gala browser tab icon. |
| **2.3.0** | Start trip in Google Maps from the leg form and the itinerary. |
| **2.2.0** | Tagline "Road Trip & Overlanding Planner" and an overlanding rig logo. |
| **2.1.0** | Fuel price and km/L carry over from the previous trip leg. |
| **2.0.0** | Tara Gala branding, editable trip title, Settings page, map pin picker, total distance, automatic fuel estimate, icon buttons in the itinerary. |
| **1.2.0** | Use my current location for the starting point. |
| **1.1.0** | Google Maps place suggestions, automatic travel time and estimated arrival. |
| **1.0.0** | Dark, responsive redesign and code cleanup. |

### Versioning guide

Every update gets a version number:

- **Patch (x.y.1):** Bug fixes and minor corrections.
- **Minor (x.1.0):** New features and improvements.
- **Major (2.0.0):** Major redesigns or significant changes.

When releasing an update, remember to change `APP_VERSION` near the top of the script in `index.html` and add a new entry to the version history.
