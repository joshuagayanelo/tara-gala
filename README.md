# 🇵🇭 Tara Gala

**Walang iwanan, puro gala lang!**

Planning your next road trip or overlanding adventure? **Tara, biyahe tayo!**

**Tara Gala** is a Road Trip & Overlanding Planner para sa mga mahilig mag-road trip, mag-overland, at mag-explore — kasama na ang mga biyahe na may RORO ferry crossings.

I-add lang ang bawat drive, ferry crossing, o transfer bilang isang trip leg. Si Tara Gala na ang bahala sa pag-compute ng distance, travel time, estimated arrival, at travel expenses mo.

It's a simple, single-file web app (`index.html`) with no build step, no backend, and no account needed. **Lahat ng trip data mo, nasa browser mo lang.**

## ✨ Features: Ano'ng meron?

### 🚙 Planuhin ang biyahe

- **Trip legs:** I-record bawat drive, ferry crossing, o major transfer. Lagyan ng route name, travel date, departure time, starting point, at destination.
- **Route names:** Bigyan ng sariling label ang bawat trip leg (halimbawa, "Manila to Baguio"). Lalabas ito sa itinerary para mas madaling makita at ma-identify ang bawat part ng journey.
- **Name your adventure:** Palitan ang trip title diretso sa page header. New trips start with **"San Tayo?"** — pangalanan ang gala mo kapag ready ka na. Mawawala ang prompt once you've renamed it.
- **Smart defaults:** Ang bagong trip leg ay automatic na magsisimula sa destination ng previous leg, gamit ang arrival date at time nito. Puwede mo pa ring baguhin ang starting point, date, at time anytime.
- **No lost work:** Kapag nag-click ka sa labas ng trip leg form o pinindot ang Esc, tatanungin ka muna kung gusto mong i-save o i-discard ang changes.
- **Route itinerary:** Automatic na naka-sort ang trip legs ayon sa date at departure time. Makikita mo ang distance, duration, estimated arrival, at cost ng bawat leg. Kung may accommodation note, makikita rin kung saan kayo mag-stay kasama ang check-in at check-out times.
- **View mode:** Buksan ang isang trip leg para makita ang complete details in read-only mode. Puwede kang pumili ng Edit o isara lang ito.
- **Trip summary line:** Makikita sa header ang date range, total number of days, at bilang ng planned legs. Example: "Dec 14 to Dec 19, 2026 (6 days) • 6 legs planned".
- **Trip summary:** Kita agad ang total expenses, total distance, total travel time, at bilang ng trip legs.

### 🗺️ Hanapin ang ruta, let's go!

Powered by Google Maps integration (optional).

- **Place suggestions:** Mag-search ng starting point at destination gamit ang autocomplete. Philippines ang default search coverage.
- **Pick on map:** Hindi mahanap ang exact location? Drop or drag a pin sa dark map para piliin ang lugar.
- **Use my location:** Gamitin ang current location ng device mo bilang starting point.
- **Automatic distance and travel time:** Automatically kinukuha ang estimated distance (km) at driving time mula sa selected places. Editable pa rin kung may gusto kang i-adjust.
- **Estimated arrival:** Kinukuwenta ang arrival time based sa departure date, time, at travel duration — kahit tumawid pa ng midnight ang biyahe.
- **Start trip in Google Maps:** Isang click lang para buksan ang route sa Google Maps, either from the trip leg form or itinerary. Sa phone, puwede itong mag-launch ng turn-by-turn navigation.

### 💸 Bantay gastos!

Para alam mo kung magkano ang kailangang budget sa bawat adventure.

- **Automatic fuel estimate:** Distance ÷ vehicle consumption (km/L) × fuel price (₱ per liter).
- **Inherited fuel values:** Ang fuel price at km/L ay automatic na kino-carry over mula sa previous trip leg, unless baguhin mo.
- **Cost categories:** I-record ang fuel, food and dining, accommodation, RORO ferry and terminal fees, at miscellaneous expenses.
- **Accommodation details:** I-note kung saan kayo mag-stay — campsite, hotel, resort, o kahit saan pa. Isama ang check-in at check-out times, kasama ang accommodation price.
- **Expense breakdown:** Makikita mo kung magkano at ilang porsiyento ang share ng bawat expense category sa total trip budget.

### 📦 Lahat ng data, nasa iyo

- **Settings page:** Manage your trip data, appearance, at Google Maps connection in one place.
- **Export to CSV:** I-download ang itinerary at expenses para madaling buksan sa spreadsheets.
- **Backup and restore:** I-save ang buong trip as a JSON file. Automatic na ginagamit ang trip title sa filename (halimbawa: `Gala-nelos-Overland-Trip-2026-backup.json`). Puwede mo ring i-restore sa ibang device o browser.
- **Local storage:** Nasa browser mo lang ang trip data. Walang account, walang backend, at walang ina-upload na trip information.

### 🎨 Your app, your style!

- **Dark and light modes:** Choose between the default low-glare dark theme and a light theme. Change your preference anytime in Settings.
- **Color combinations:** Pumili mula sa five additional color combinations in each mode, or reset to the default colors.
- **Responsive layout:** Works on desktop, tablet, at mobile.
- **Mobile-friendly itinerary:** Sa phone, cards ang display ng itinerary at bottom sheets naman ang forms para mas madaling gamitin. Each itinerary card also displays its leg number at the top for easier navigation.

---

## 🚀 Paano magsimula?

1. Buksan ang `index.html` sa browser mo, or i-host ang repository gamit ang GitHub Pages.
2. Click **Add trip leg** at ilagay ang route details.
3. Optional: I-enable ang Google Maps integration para sa autocomplete, map pins, at automatic distance and travel time.

**Good news:** Gumagana ang Tara Gala kahit walang Google Maps API key. Puwede mong manual na ilagay ang places, distance, at travel time.

## 🗺️ Google Maps setup

Gusto mo ng place suggestions, map pins, current-location names, at automatic distance? Kailangan mo ng Google Maps API key.

1. Pumunta sa [Google Cloud Console](https://console.cloud.google.com/) at gumawa ng project at API key.
2. I-enable ang mga sumusunod na APIs:
   - Maps JavaScript API
   - Places API (New)
   - Routes API
   - Geocoding API (optional — para ma-display ang pinned at current locations bilang addresses)
3. I-restrict ang API key:
   - **Application restrictions:** Piliin ang Websites at idagdag ang website address mo. Example: `https://your-username.github.io/*`.
   - **API restrictions:** Piliin ang Restrict key at i-allow lang ang Google Maps APIs na ginagamit ng Tara Gala.
4. Sa app, pumunta sa **Settings → Google Maps**, i-paste ang API key, at click **Save key**.

### 🔐 API key security

Tara Gala uses a browser-based Google Maps integration, so your API key is loaded by the browser and may be visible to users who inspect the app or its network requests.

This is expected for Google Maps JavaScript API applications. The key is not a private password, but it must be properly restricted to prevent unauthorized use.

For security:

- **Restrict websites:** Allow only your GitHub Pages domain and any custom domain you use.
- **Restrict APIs:** Allow only the Google Maps APIs required by Tara Gala.
- **Monitor usage:** Regularly check your Google Cloud API usage and billing.
- **Control costs:** Configure API quotas where supported and set billing notifications.

The key is stored in your browser and is not committed to the source code or GitHub repository. However, browser storage does not make it secret.

**Never use an unrestricted API key in a publicly accessible app.**

Keys restricted to a website address don't work when `index.html` is opened directly from your computer, so use a hosted page or a local server. If testing locally, configure an appropriate localhost website restriction as well.

## 🌐 Deploy with GitHub Pages

Gustong i-share ang Tara Gala online? Sundan lang ang steps na ito:

1. Ilagay ang `index.html` sa root folder ng GitHub repository mo, under the `main` branch.
2. Pumunta sa **Settings → Pages**.
3. Sa **Build and deployment**, piliin ang **Deploy from a branch**.
4. Piliin ang `main` branch at `/ (root)`, then save.
5. After a minute or two, available na ang app mo sa:

   `https://<your-username>.github.io/<repository-name>/`

Tara na, ready na ang next adventure mo!

## ⚠️ Bago bumiyahe, tandaan!

- **RORO travel time:** Ang Google Maps driving estimate ay maaaring hindi kasama ang RORO crossing, terminal waiting time, at rest stops. I-adjust ang travel time manually para mas realistic ang estimated arrival.
- **Accommodation details:** I-check ang check-in at check-out times para maiwasan ang scheduling conflicts sa itinerary.
- **Backup your data:** Nasa browser local storage ang trip data. Kapag nag-clear ka ng site data, mabubura rin ito. Regular na mag-click ng **Save backup**.
- **Current location:** Kailangan ng secure HTTPS connection para ma-access ng browser ang location mo. Kaya mas reliable ang **Use my location** sa GitHub Pages kaysa sa locally opened file.
- **Google Maps billing:** May charges ang Google Maps services depende sa usage. I-check ang latest pricing at free usage limits ng Google Cloud account mo. Remember to monitor your usage and configure API restrictions.

## 🛠️ Built with

- Plain HTML
- CSS
- JavaScript
- Google Maps JavaScript API (Places, Routes, Geocoding, and Maps libraries — optional)

No frameworks. No build tools. Just one `index.html` file.

## 📌 Version history

The current app version is displayed in the app footer and on the Settings page.

| Version | Changes |
|---|---|
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

Every update gets a new version number:

- **Patch (`x.y.1`)** — Bug fixes and small improvements.
- **Minor (`x.1.0`)** — New features and functionality.
- **Major (`3.0.0`)** — Major redesigns or significant changes.

Remember to update `APP_VERSION` near the top of the script in `index.html` and add a new row to the version history.

---

## ❤️ Tara na!

Planuhin ang biyahe. Bantayan ang gastos. Sulitin ang bawat gala.

**Less hassle sa planning, more time sa adventure!**

**Tara Gala — Bawat biyahe, may kuwento.** 🇵🇭
