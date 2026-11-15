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
| **3.5.1** | Improved completed-leg animations: cards slide away, the remaining page content glides into place, the Completed legs panel opens and closes smoothly, and completed-leg rows animate into view one by one. |
| **3.5.0** | Added the ability to mark trip legs as complete. Completed legs move into a collapsible "Completed legs" section where they can be viewed, restored as incomplete, or deleted. Added an undo option after marking a leg as complete. |
| **3.4.0** | The map picker now has a place search box and a My Location button, in addition to tapping or dragging the pin. |
| **3.3.0** | Smooth open and close motion for the leg view and all other dialogs. On phones and tablets the leg view slides up like a sheet, and its sections fade in one after another. |
| **3.2.1** | Removed the blue tap flash on mobile. Cards and buttons still open and respond to taps. |
| **3.2.0** | Tap or click an itinerary row or card to open the leg view. The leg view fills the screen
