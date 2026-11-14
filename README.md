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
- **Trip Legs:** Add every drive, ferry crossing, or major transfer with dates, departure times, starting points, and destinations.
- **Trip Name:** Give your adventure a name! Rename your trip anytime (e.g. "Gala-nelos Overland Trip 2026").
- **Route Itinerary:** Keep your legs organized by date and departure time, with distance, duration, estimated arrival, and costs.
- **Trip Summary:** See your total gastos, distance, travel time, and number of trip legs at a glance.

### 🗺️ Hanapin ang tamang ruta
- **Place Suggestions:** Search starting points and destinations with Google Maps autocomplete (Philippines by default).
- **Pick on Map:** Drop or drag a pin on the map. No need to memorize addresses!
- **Use My Location:** Start your adventure from where you are.
- **Auto Distance & Travel Time:** Automatically calculate driving distance (km) and travel time. Need adjustments? Edit them anytime.
- **Estimated Arrival:** Know when you'll arrive, even when your biyahe crosses midnight.
- **Open in Google Maps:** One click and you're ready to navigate!

### 💸 Bantay gastos!
- **Fuel Calculator:** Automatically estimate fuel costs using distance, vehicle consumption (km/L), and fuel price (₱/liter).
- **Carry-over Fuel Settings:** Fuel price and vehicle consumption carry over from your previous trip leg. Less encoding, less hassle!
- **Expense Categories:** Track fuel, food, accommodation, RORO and terminal fees, and miscellaneous expenses.
- **Expense Breakdown:** See where your budget goes. Para walang gulatan!

### 📦 Lahat ng data, nasa iyo
- **Settings:** Manage your trip data and Google Maps connection in one place.
- **Export to CSV:** Download your itinerary and expenses for spreadsheets.
- **Backup & Restore:** Save your entire trip as a JSON file and restore it on another device or browser.
- **Local Storage:** Your trip data stays in your browser. Walang account, walang backend, walang ina-upload!

### 🌙 Simple lang, pero sulit
- **Dark Mode:** Easy-on-the-eyes interface for those late-night planning sessions.
- **Responsive Design:** Works on desktop, tablet, and mobile.
- **Mobile-friendly:** Itineraries become easy-to-read cards, while forms open as convenient bottom sheets.

---

## 🚀 Paano magsimula?

Ready na ba? Let's get your next adventure rolling!

1. Open `index.html` in your browser, or deploy it using GitHub Pages.
2. Click **Add Trip Leg**.
3. Fill in your starting point, destination, schedule, and expenses.
4. Add more legs until your entire adventure is mapped out.
5. Optional: Connect Google Maps for automatic place suggestions and route calculations.

**Walang Google Maps API key? No problem!** You can still manually enter locations, distances, and travel times.

---

## 🗺️ Google Maps setup

Gusto mo ng automatic place suggestions, map pins, and route calculations? You'll need a Google Maps API key.

1. Visit [Google Cloud Console](https://console.cloud.google.com/).
2. Create a project and generate an API key.
3. Enable these APIs:
   - Maps JavaScript API
   - Places API (New)
   - Routes API
   - Geocoding API (optional, for address details of pinned and current locations)
4. Restrict your API key to the required APIs and your website domain (e.g. `https://your-username.github.io/*`).
5. Open **Settings → Google Maps**, paste your API key, and click **Save Key**.

Your API key is stored only in your browser. It is never written into the code or repository.

**Heads up!** Website-restricted keys won't work when opening `index.html` directly from your computer. Use GitHub Pages or a local server instead.

---

## 🌐 Deploy with GitHub Pages

Gusto mo nang i-share ang Tara Gala? Let's put it online!

1. Upload `index.html` to the root of your GitHub repository on the `main` branch.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose `main` and `/ (root)`.
5. Hit **Save** and wait for deployment.

Your app will be live at:

`https://<your-username>.github.io/<repository-name>/`

Ayos! Your very own trip planner is now online. 🎉

---

## ⚠️ Bago bumiyahe, tandaan!

A few things to keep in mind:

- **RORO & Rest Stops:** Google Maps driving estimates may not include ferry crossings, terminal waiting times, or rest stops. Add these to your travel time manually.
- **Backup Your Trips:** Your data lives in your browser's local storage. Clearing browser data may erase your trips, so use **Save Backup** regularly.
- **Location Access:** Browsers require HTTPS for location services. GitHub Pages supports this.
- **Google Maps Costs:** Google Maps services may incur charges. Check Google's latest pricing and free usage limits.

---

## 🛠️ Built with

- HTML5
- CSS3
- Vanilla JavaScript
- Google Maps JavaScript API (optional)

No frameworks. No build process. No complicated setup.

Just one `index.html,` and you're ready to gala!

---

## ❤️ Tara na!

**Planuhin ang biyahe. Bantayan ang gastos. Sulitin ang bawat gala.**

Made with ❤️ for Filipino road trippers, campers, overlanders, and adventure-loving families.

**Tara Gala! Bawat biyahe, may kuwento.** 🇵🇭🏕️
