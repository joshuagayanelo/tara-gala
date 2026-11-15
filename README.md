# 🇵🇭 Tara Gala!

**Walang iwanan, puro gala lang!** 🏕️🚙

Planning your next road trip or overlanding adventure? Tara, biyahe tayo!

**Tara Gala** is your Filipino-inspired **Road Trip & Overlanding Planner**. Whether you're cruising along highways, exploring mountain trails, or hopping between islands via RORO, we've got your trip planning covered.

Plan your routes, bantayan ang gastos, estimate your fuel, organize your RORO crossings, and keep your entire adventure in one place.

Less hassle sa planning, more time sa gala!

Built for Filipino road trippers, campers, overlanders, and families who love exploring the Philippines. 🇵🇭

## ✨ Features: Ano'ng meron?

### 🚙 Planuhin ang biyahe

- **Trip legs:** I-log bawat drive, ferry crossing, or major transfer. Add a route name, date, departure time, starting point, and destination.
- **Route names:** Lagyan ng sariling pangalan ang bawat leg (halimbawa, "Manila to Baguio"). Lalabas ito as a highlighted label sa itinerary.
- **Editable trip title:** Pangalanan ang adventure mo right from the page header. New trips start with **"San Tayo?"** and a prompt to name your gala. Mawawala ang prompt once you rename it.
- **Smart defaults:** Ang next leg ay automatic na magsisimula sa destination ng previous leg, gamit ang arrival date and time nito. Editable pa rin lahat.
- **No lost work:** Kapag nag-click ka outside the leg form or pinindot ang Esc, tatanungin ka kung gusto mong i-save or i-discard ang changes.
- **Organized itinerary:** Automatically sorted by date and departure time. Makikita ang distance, duration, estimated arrival, and cost for every leg. May accommodation details din kung saan ka mag-stay, kasama ang check-in and check-out times.
- **Completed legs:** Mark a trip leg as complete kapag natapos na ang biyahe. Lilipat ito sa collapsible **Completed legs** section para hindi na makasagabal sa active itinerary. Puwede mo itong i-view, i-restore as incomplete, or i-delete. May undo option din right after marking a leg as complete.
- **View mode:** Click an itinerary row, tap a card, or use the eye icon para makita ang complete details ng isang leg in read-only mode. Choose Edit or close kapag tapos na. Sa phones and tablets, full-screen ang view.
- **Floating Add leg button:** Hindi mo na kailangang mag-scroll pabalik sa taas. The Add leg button stays at the bottom right habang nagba-browse ka ng itinerary.
- **Trip summary line:** Kita agad ang date range, total days, and number of planned legs. Example: "Dec 14 to Dec 19, 2026 (6 days) • 6 legs planned".
- **Trip summary:** Check your total expenses, distance, travel time, and number of legs at a glance.

### 🗺️ Hanapin ang ruta, let's go!

- **Place suggestions:** Search your starting point and destination with autocomplete. Philippines ang default search coverage.
- **Pick on map:** Search for a place, use your current location, or drop and drag a pin on the map. No need to type everything manually.
- **Use my location:** Gamitin ang current location ng device mo as your starting point.
- **Automatic distance and travel time:** Automatically calculates driving distance in kilometers and estimated travel time based on your selected places. Puwede mo pa ring i-edit manually.
- **Estimated arrival:** Automatically calculates arrival time based on departure date, time, and travel duration — kahit tumawid pa ng midnight ang biyahe.
- **Start trip in Google Maps:** One click lang para buksan ang route sa Google Maps, either from the leg form or itinerary. Sa phone, puwede itong mag-launch ng turn-by-turn navigation.

### 💸 Bantay gastos!

- **Automatic fuel estimate:** Calculates fuel cost using distance ÷ vehicle consumption (km/L) × fuel price per liter.
- **Inherited fuel values:** Automatically carries over fuel price and vehicle consumption from the previous leg, unless you change them.
- **Expense categories:** Track fuel, food and dining, accommodation, RORO ferry and terminal fees, and miscellaneous expenses.
- **Accommodation details:** Record kung saan ka mag-stay — campsite, hotel, or resort — including check-in and check-out times, alongside the accommodation price.
- **Expense breakdown:** Makikita mo kung magkano ang share ng bawat category sa total trip budget.

### 📦 Lahat ng data, nasa iyo

- **Settings page:** Manage your trip data and Google Maps connection in one place.
- **Export to CSV:** Download your itinerary and expenses para madaling buksan sa spreadsheets.
- **Backup and restore:** Save your entire trip as a JSON backup file named after your trip title. Example: `Gala-nelos-Overland-Trip-2026-backup.json`. Puwede mo rin itong i-restore sa ibang device or browser.
- **Local storage:** All your trip data stays in your browser. Walang account, walang backend, at walang ina-upload sa server.

### 🌙 Simple lang, pero sulit

- **Dark and light modes:** Low-glare dark mode ang default, pero puwede kang mag-switch to light mode sa Settings.
- **Color combinations:** Choose from five extra color combinations in each mode, or reset to the default colors.
- **Responsive layout:** Designed for desktop, tablet, and mobile. Sa phones, cards ang itinerary at bottom sheets ang forms para mas madaling gamitin.

## 🚀 Paano magsimula?

1. Open `index.html` sa browser mo, or i-host ang repository using GitHub Pages (instructions below).
2. Click **Add trip leg** and fill in your route details.
3. Optional: Connect Google Maps para sa place suggestions, map picker, and automatic distance and travel time.

**Good news:** Gumagana ang Tara Gala kahit walang Google Maps integration. Puwede mong i-type manually ang places, distance, and travel time.

## 🗺️ Google Maps setup

Para gumana ang place suggestions, map pins, current-location names, and automatic distance, kailangan mo ng Google Maps API key.

1. Pumunta sa [Google Cloud Console](https://console.cloud.google.com/), create a project, and generate an API key.
2. Enable these APIs:
   - Maps JavaScript API
   - Places API (New)
   - Routes API
   - Geocoding API (optional, for address labels of pinned and current locations)
3. Restrict your API key:
   - **Application restrictions:** Choose Websites and add your GitHub Pages domain, custom domain, or localhost address for local testing.
   - **API restrictions:** Choose Restrict key and allow only the APIs your app uses.
4. Sa Tara Gala, open **Settings → Google Maps**, paste your API key, then click **Save key**.

**Important security reminders:**

- The API key is stored in your browser, not in the source code or GitHub repository.
- However, a browser-based API key is still visible to visitors who inspect the app or its network requests. Treat it as a restricted public key, not a secret.
- Always apply website and API restrictions to reduce unauthorized use.
- Monitor your Google Cloud usage and billing. Set quotas and billing alerts where available.
- A website-restricted key won't work when opening `index.html` directly using `file://`. Use GitHub Pages or a local development server instead.
- If you later add server-side Google web-service requests, review the architecture and use a backend proxy with private credentials where required.

Google Maps services may incur charges depending on usage and your Google Cloud account. Check the current pricing and free usage limits before enabling the APIs.

## 🌐 Deploy with GitHub Pages

Gusto mong ma-access ang Tara Gala online, kahit saan ka mag-plano? You can host it for free using GitHub Pages.

1. Create a GitHub repository.
2. Upload `index.html` to the root of your repository on the `main` branch.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, select **Deploy from a branch**.
5. Choose `main` and `/ (root)`, then save.
6. After deployment, your app will be available at:

   `https://<your-username>.github.io/<repository-name>/`

That's it! Your Tara Gala planner is now online. 🚙

## ⚠️ Bago bumiyahe, tandaan!

- Google's driving estimates may not include RORO crossings, terminal waiting time, boarding, or rest stops. Add the extra time manually para mas realistic ang arrival estimates.
- Your trip data is saved in your browser's local storage. Kapag nag-clear ka ng browser site data, puwedeng mawala ang saved trips. Use **Save backup** regularly!
- Browser location access requires a secure HTTPS connection. **Use my location** works on GitHub Pages but may not work when opening a local file.
- Google Maps services may be billed depending on your usage. Check current pricing, free usage limits, and billing settings.
- Keep your API key restricted to your website and the APIs you actually use. Never assume that browser storage makes an API key private.

## 🛠️ Built with

- HTML5
- CSS3
- Vanilla JavaScript
- Google Maps JavaScript API (Maps, Places, Routes, and Geocoding libraries) — optional

No frameworks. No build process. No backend. No database.

Just one `index.html` file and you're ready to gala!

## 📌 Version history

The current version is displayed in the app footer and on the Settings page.

| Version | Changes |
|---|---|
| **3.5.0** | Added the ability to mark trip legs as complete. Completed legs move into a collapsible "Completed legs" section where they can be viewed, restored as incomplete, or deleted. Added an undo option after marking a leg as complete. |
| **3.4.0** | The map picker now has a place search box and a My Location button, in addition to tapping or dragging the pin. |
| **3.3.0** | Smooth open and close motion for the leg view and all other dialogs. On phones and tablets the leg view slides up like a sheet, and its sections fade in one after another. |
| **3.2.1** | Removed the blue tap flash on mobile. Cards and buttons still open and respond to taps. |
| **3.2.0** | Tap or click an itinerary row or card to open the leg view. The leg view fills the screen in card view. The Add leg button floats at the bottom right while scrolling. Smooth transitions on all buttons. |
| **3.1.0** | "Estimated costs" renamed to "Expenses". Food & dining, RORO ferry & terminal and Miscellaneous amounts are shown in the itinerary (₱0 in the table, hidden on cards when empty). Cards now take over from the table at 1400 px and below, and the expenses panel sits below the itinerary. |
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

Every update gets a new version number:

- **Patch (x.y.1):** Bug fixes and minor improvements.
- **Minor (x.1.0):** New features and enhancements.
- **Major (2.0.0):** Major redesigns or significant changes.

When releasing an update, remember to change `APP_VERSION` near the top of the script in `index.html` and add a new row to the version history above.

## ❤️ Tara na!

**Planuhin ang biyahe. Bantayan ang gastos. Sulitin ang bawat gala.**

Made with ❤️ for Filipino road trippers, campers, overlanders, and adventure-loving families.

**Tara Gala! Bawat biyahe, may kuwento.** 🇵🇭🏕️
