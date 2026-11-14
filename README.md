# tara-gala
Your Filipino road trip and overlanding companion. Plan. Biyahe. Gala.

# 🇵🇭 Tara Gala!

**Walang iwanan, puro gala lang!** 🏕️🚙

Planning your next road trip or overlanding adventure? Tara, let's go!

**Tara Gala** is your all-in-one road trip planner. Whether you're cruising through highways, exploring scenic mountain roads, or hopping between islands via RORO, we've got your trip planning covered.

Plan your routes, track your gastos, estimate fuel costs, organize ferry crossings, and keep your entire adventure in one place. Less hassle sa planning, more time sa gala!

Built for Filipino road trippers, campers, overlanders, and families who love exploring the Philippines. 🇵🇭

## ✨ What's inside?

### 🚙 Plan your biyahe
- Add every drive, ferry crossing, and transfer as a trip leg.
- Customize your trip name and organize your itinerary.
- Track distances, travel times, arrival times, and estimated costs.
- See your total distance, travel time, expenses, and trip legs at a glance.

### 🗺️ Know your ruta
- Search locations with Google Maps suggestions.
- Drop or drag pins to pick your destinations.
- Use your current location as your starting point.
- Automatically calculate driving distance and travel time.
- Open your routes directly in Google Maps.

### 💸 Bantay gastos!
- Automatically estimate fuel expenses based on km/L and fuel price.
- Carry over fuel settings from your previous trip leg.
- Track gastos for fuel, food, accommodation, RORO fees, and more.
- View your expense breakdown so walang gulatan sa budget!

### 📦 Your trip, your data
- Export your itinerary and expenses to CSV.
- Back up and restore your trips using JSON files.
- Manage your Google Maps API key in Settings.
- All trip data stays in your browser. Walang account, walang backend!

### 🌙 Made for every screen
- Clean, eye-friendly dark mode.
- Responsive layout for desktop, tablet, and mobile.
- Mobile-friendly itinerary cards and bottom-sheet forms.

## 🚀 Getting started

1. Open `index.html` in your browser.
2. Hit **Add Trip Leg**.
3. Enter your starting point, destination, schedule, and expenses.
4. Repeat for every leg of your adventure.
5. Optional: Connect Google Maps for automatic routes and distance calculations.

**No Google Maps key? No problem!** You can still manually enter locations, distances, and travel times.

## 🗺️ Google Maps setup

Want automatic place suggestions, map pins, and route calculations? You'll need a Google Maps API key.

1. Visit [Google Cloud Console](https://console.cloud.google.com/).
2. Create a project and generate an API key.
3. Enable the following APIs:
   - Maps JavaScript API
   - Places API (New)
   - Routes API
   - Geocoding API (optional)
4. Restrict your API key to the required APIs and your website domain (e.g. `https://your-username.github.io/*`).
5. Open **Settings → Google Maps**, paste your API key, and hit **Save Key**.

Your API key is stored in your browser, not in the repository or source code.

**Note:** Website-restricted keys won't work when opening `index.html` directly. Use GitHub Pages or a local server instead.

## 🌐 Deploy with GitHub Pages

Want to take Tara Gala online? Here's how:

1. Upload `index.html` to the root of your GitHub repository on the `main` branch.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose `main` and `/ (root)`.
5. Save and wait for deployment.

Your app will be live at:

`https://<your-username>.github.io/<repository-name>/`

Ayos! Your very own trip planner is now online. 🎉

## ⚠️ A few things to remember

- Google Maps driving estimates don't automatically account for RORO crossings, terminal queues, or rest stops. Add these to your travel time manually.
- Your trip data is stored locally in your browser. Clearing browser data may erase your trips, so make regular backups.
- Location services require HTTPS. GitHub Pages supports this.
- Google Maps API usage may incur charges. Check Google's current pricing and free usage limits.

## 🛠️ Built with

- HTML5
- CSS3
- Vanilla JavaScript
- Google Maps JavaScript API (optional)

No frameworks. No build process. No complicated setup. Just one `index.html` and you're ready to gala!

---

**Tara Gala!** 🏕️

*Planuhin ang biyahe. Bantayan ang gastos. Sulitin ang bawat gala.*

Made with ❤️ for Filipino road trippers and overlanding enthusiasts.
