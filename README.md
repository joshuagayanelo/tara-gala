# 🇵🇭 Tara Gala!

**Walang iwanan, puro gala lang!** 🏕️🚙

Planning your next road trip or overlanding adventure? Tara, biyahe tayo!

**Tara Gala** is your Filipino-inspired **Road Trip & Overlanding Planner**. Whether you're cruising along highways, exploring mountain trails, or hopping between islands via RORO, we've got your trip planning covered.

Plan your routes, bantayan ang gastos, estimate your fuel, organize your RORO crossings, and keep your entire adventure in one place.

Less hassle sa planning, more time sa gala!

Built for Filipino road trippers, campers, overlanders, and families who love exploring the Philippines. 🇵🇭

---

## ✨ Features: Ano'ng meron?

### 🚙 Planuhin ang biyahe

- **Trip Legs:** Add every drive, ferry crossing, or major transfer with a route name, date, departure time, starting point, and destination.
- **Route Names:** Give each trip leg a highlighted label (e.g. "Manila to Baguio") that appears above the route in your itinerary.
- **San Tayo?:** Every new trip starts with a friendly "San Tayo?" title. Give your adventure a name anytime! The naming prompt disappears once you rename it.
- **Smart Defaults:** Your next trip leg automatically starts from the previous leg's destination and inherits its estimated arrival date and time. Less encoding, less hassle! You can still change these details anytime.
- **No Lost Work:** Click outside the leg form or press Esc, and Tara Gala asks whether you want to save or discard your changes.
- **Route Itinerary:** Keep your trip legs organized by date and departure time. See each leg's distance, duration, estimated arrival, and cost. May accommodation details din, including where you're staying and your check-in/check-out times.
- **View Leg Details:** Click an itinerary row, tap a card, or use the eye icon to view all leg details without accidentally editing anything. Choose Edit when you need to make changes. On phones and tablets, the leg view fills the screen for easier viewing.
- **Floating Add Leg Button:** No need to scroll back to the top! The Add Leg button stays at the bottom right while you browse your itinerary. Add another stop anytime.
- **Trip Summary:** See your travel date range, total days, and number of planned legs right in the header. Example: "Dec 14 to Dec 19, 2026 (6 days) • 6 legs planned".
- **Trip Overview:** Check your total expenses, distance, travel time, and number of trip legs at a glance.

### 🗺️ Hanapin ang ruta, let's go!

- **Place Suggestions:** Search starting points and destinations with Google Maps autocomplete (Philippines by default).
- **Smarter Map Picker:** Find a place using the search box, jump to your current location with the My Location button, or simply tap and drag the pin to your preferred spot. More ways to pinpoint your destination!
- **Use My Location:** Set the starting point from your device's current location.
- **Auto Distance & Travel Time:** Automatically calculate driving distance (km) and estimated travel time based on your selected places. Need adjustments? Edit them anytime.
- **Estimated Arrival:** Know when you'll arrive, even when your biyahe crosses midnight.
- **Start Trip in Google Maps:** Ready to hit the road? Launch your route directly from the trip leg form or itinerary. On mobile, it opens turn-by-turn navigation. No more switching apps just to find your destination!

### 💸 Bantay gastos!

- **Fuel Calculator:** Automatically estimate fuel costs using distance, vehicle consumption (km/L), and fuel price (₱/liter).
- **Carry-over Fuel Settings:** Fuel price and vehicle consumption carry over from your previous trip leg. Less encoding, less hassle!
- **Expense Categories:** Track fuel, food and dining, accommodation, RORO ferry and terminal fees, and miscellaneous expenses.
- **Accommodation Tracker:** Record where you're staying — campsite, hotel, or resort — including check-in and check-out times, alongside the accommodation cost.
- **Expense Breakdown:** See how much each expense category contributes to your total trip budget. Para walang gulatan!

### 📦 Lahat ng data, nasa iyo

- **Settings:** Manage your trip data and Google Maps connection in one place.
- **Export to CSV:** Download your itinerary and expenses for spreadsheets and further analysis.
- **Backup & Restore:** Save your entire trip as a JSON file, with the filename based on your trip title (e.g. `Gala-nelos-Overland-Trip-2026-backup.json`). Restore it on another device or browser.
- **Local Storage:** Your trip data stays in your browser. Walang account, walang backend, walang ina-upload!

### 🌙 Simple lang, pero sulit

- **Dark & Light Modes:** Choose a low-glare dark interface by default, or switch to light mode in Settings.
- **Color Combinations:** Pick from five additional color combinations in each mode, or reset to the default colors.
- **Responsive Design:** Works on desktop, tablet, and mobile.
- **Mobile-friendly Itinerary:** On phones, your itinerary becomes easy-to-read cards, while forms open as convenient bottom sheets.
- **Roomier Itinerary:** More breathing room for your trip details! Table values stay neatly on one line (except routes), and the expenses panel moves below the itinerary on screens narrower than 1440px.
- **Smooth Transitions:** Buttons have smooth transitions for a more polished experience.
- **No Blue Tap Flash:** Removed the blue tap highlight on mobile. Cards and buttons still respond normally when tapped.
- **Smoother Dialog Animations:** Opening and closing the leg view and other dialogs now feels smoother. On phones and tablets, the leg view slides up like a sheet, while its sections fade in one after another.

---

## 🚀 Paano magsimula?

Ready na ba? Let's get your next adventure rolling!

1. Open `index.html` in your browser, or deploy it using GitHub Pages.
2. Click **Add Trip Leg**.
3. Fill in your route name, starting point, destination, schedule, and expenses.
4. Add more legs until your entire adventure is mapped out.
5. Optional: Connect Google Maps for automatic place suggestions, route calculations, map pins, and navigation.

**Walang Google Maps API key? No problem!** You can still manually enter locations, distances, and travel times. Tara Gala works even without Google Maps integration!

---

## 🗺️ Google Maps setup

Gusto mo ng automatic place suggestions, map pins, and route calculations? You'll need a Google Maps API key.

### 1. Create your API key

1. Visit [Google Cloud Console](https://console.cloud.google.com/).
2. Create a project or select an existing one.
3. Generate an API key under APIs & Services → Credentials.

### 2. Enable the required APIs

Enable these APIs for your project:

- Maps JavaScript API
- Places API (New)
- Routes API
- Geocoding API (optional, for address details of pinned and current locations)

### 3. Restrict your API key

For security, configure your API key restrictions before publishing your app.

**Application restrictions:**

- Select **Websites**.
- Add your GitHub Pages address (e.g. `https://your-username.github.io/*`).
- If you're using a custom domain, add that domain too.
- If testing locally through a local server, add the appropriate localhost referrer.

**API restrictions:**

- Select **Restrict key**.
- Allow only the Google Maps APIs your app actually uses.

It's also a good idea to monitor API usage, configure available quotas, and set up billing alerts.

### 4. Connect your key to Tara Gala

1. Open the app.
2. Go to **Settings → Google Maps**.
3. Paste your API key.
4. Click **Save Key**.

Your API key is stored in your browser and is not written into the app's source code or repository.

**Heads up! Security matters!** A browser-based Google Maps API key is visible to visitors who inspect your website or network requests. Storing it in browser storage does not make it secret. Always apply website and API restrictions before publishing. Never use an unrestricted API key in a public repository or website.

Website-restricted keys generally won't work when opening `index.html` directly from your computer using a `file://` address. Use GitHub Pages or a local development server instead.

Google Maps services may incur charges depending on usage. Check Google's latest pricing, free usage limits, and billing requirements.

---

## 🌐 Deploy with GitHub Pages

Gusto mo nang ma-access ang Tara Gala online? Let's put it on the road!

### 1. Create a GitHub repository

Upload `index.html` to the root of your GitHub repository on the `main` branch.

### 2. Enable GitHub Pages

1. Open your repository.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose `main` and `/ (root)`.
5. Hit **Save** and wait for deployment.

### 3. Open your app

Your app will be live at:

`https://<your-username>.github.io/<repository-name>/`

Ayos! Your very own trip planner is now online. 🎉

---

## ⚠️ Bago bumiyahe, tandaan!

- **RORO & Rest Stops:** Google Maps driving estimates may not include ferry crossings, terminal waiting times, boarding, or rest stops. Add these to your travel time manually for a more realistic arrival estimate.
- **Backup Your Trips:** Your data lives in your browser's local storage. Clearing browser or website data may erase your trips, so use **Save Backup** regularly.
- **Location Access:** Browsers generally require HTTPS for location services. GitHub Pages supports this, but opening the app directly from a local file may not.
- **Google Maps Costs:** Google Maps services may incur usage-based charges. Check Google's latest pricing and free usage limits.
- **API Key Security:** Browser-based API keys are visible to website visitors. Always restrict your key to your website and the APIs your app uses.

---

## 🛠️ Built with

- HTML5
- CSS3
- Vanilla JavaScript
- Google Maps JavaScript API (optional)

No frameworks. No build process. No complicated setup.

Just one `index.html` and you're ready to gala!

---

## 📌 Version history

The current app version is displayed in the footer and Settings page.

| Version | Changes |
|---|---|
| **3.4.0** | The map picker now includes a place search box and a My Location button, in addition to tapping or dragging the pin. |
| **3.3.0** | Added smooth opening and closing animations for the leg view and all other dialogs. On phones and tablets, the leg view slides up like a sheet, with sections fading in sequentially. |
| **3.2.1** | Removed the blue tap flash on mobile. Cards and buttons still open and respond to taps. |
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

### 🔢 Versioning

Every update gets a version number:

- **Patch (x.y.1):** Bug fixes and minor improvements.
- **Minor (x.1.0):** New features and enhancements.
- **Major (2.0.0):** Big redesigns or significant changes.

Update `APP_VERSION` near the top of `index.html` and add a new entry to the version history whenever you release an update.

---

## ❤️ Tara na!

**Planuhin ang biyahe. Bantayan ang gastos. Sulitin ang bawat gala.**

Made with ❤️ for Filipino road trippers, campers, overlanders, and adventure-loving families.

**Tara Gala! Bawat biyahe, may kuwento.** 🇵🇭🏕️
