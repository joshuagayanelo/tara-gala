# Tara Gala

**Tara Gala** is a Road Trip & Overlanding Planner for overland trips, including routes that use RORO ferries. Add each drive or ferry crossing as a trip leg, and the app works out the distance, travel time, arrival time and estimated costs for you.

It is a single `index.html` file with no build step, no backend and no account. Your trip data stays in your browser.

## Features

### Trip planning
- **Trip legs:** log every drive, ferry or major transfer with a date, departure time, starting point and destination.
- **Editable trip title:** rename the trip (for example "Gala-nelos Overland Trip 2026") right from the page header.
- **Route itinerary:** legs are sorted by date and departure time, with distance, duration, estimated arrival and cost for each leg.
- **Trip summary:** total expenses, total distance, total travel time and number of legs at a glance.

### Google Maps integration
- **Place suggestions:** search for the starting point and destination with autocomplete (limited to the Philippines by default).
- **Pick on map:** drop or drag a pin on a dark map instead of typing a place name.
- **Use my location:** set the starting point from your device's current location.
- **Automatic distance and travel time:** total distance (km) and driving time are filled in from the selected places. Both can still be edited by hand.
- **Estimated arrival:** calculated from the date, departure time and travel time, including legs that cross midnight.
- **Open in Google Maps:** view any route in Google Maps with one click.

### Cost estimates
- **Automatic fuel estimate:** distance ÷ vehicle consumption (km/L) × fuel price (₱ per liter).
- **Inherited fuel values:** fuel price and km/L carry over from the previous trip leg unless you change them.
- **Cost categories:** fuel, food and dining, accommodation, RORO ferry and terminal fees, and miscellaneous.
- **Expense breakdown:** see the share of each category in the total trip budget.

### Data and settings
- **Settings page:** manage your data and your Google Maps connection in one place.
- **Export to CSV:** download the itinerary and costs for spreadsheets.
- **Backup and restore:** save the whole trip as a JSON file and restore it on another device or browser.
- **Local storage:** everything is saved in your browser, so nothing is uploaded anywhere.

### Design
- **Dark theme:** a low-glare dark interface that is easier on the eyes.
- **Responsive layout:** works on desktop, tablet and mobile. On phones the itinerary becomes cards and forms open as bottom sheets.

## Getting started

1. Open `index.html` in a browser, or host the repository with GitHub Pages (see below).
2. Click **Add trip leg** and fill in the route.
3. Optional: turn on the Google Maps features (see the next section).

The app works without Google Maps. You can type places, distance and travel time by hand.

## Setting up Google Maps

Place suggestions, map pins, current-location names and automatic distance need a Google Maps API key.

1. In [Google Cloud Console](https://console.cloud.google.com/), create a project and an API key.
2. Enable these APIs for the project:
   - Maps JavaScript API
   - Places API (New)
   - Routes API
   - Geocoding API (optional, shows pinned and current locations as addresses)
3. Restrict the key to those APIs and to your website address, for example `https://your-username.github.io/*`.
4. In the app, open **Settings → Google Maps**, paste the key and click **Save key**.

The key is stored only in your browser. It is never written into the code or the repository.

Keys restricted to a website address don't work when `index.html` is opened directly from your computer, so use a hosted page or a local server.

## Deploying with GitHub Pages

1. Put `index.html` in the root of the repository on the `main` branch.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then select `main` and `/ (root)`.
4. After a minute or two the app is available at `https://<your-username>.github.io/<repository-name>/`.

## Things to know

- Google's driving estimate may not include RORO crossings, terminal waiting time or rest stops. Add that time to the travel time yourself.
- Data lives in your browser's local storage. Clearing site data removes it, so use **Save backup** regularly.
- Browsers share your location only on secure (HTTPS) pages, so **Use my location** works on GitHub Pages but may not work from a local file.
- Google Maps services are billed by Google. Check the current pricing and free usage limits for your account.

## Tech

Plain HTML, CSS and JavaScript in a single file. Uses the Google Maps JavaScript API (Places, Routes, Geocoding and Maps libraries) when a key is provided.
