# 🇵🇭 Tara Gala

**Walang iwanan, puro gala lang!**

Planning your next road trip or overlanding adventure? **Tara, biyahe tayo!**

**Tara Gala** is a Road Trip & Overlanding Planner para sa mga mahilig mag-road trip, mag-overland, at mag-explore — kasama na ang mga biyahe na may RORO ferry crossings.

I-add lang ang bawat drive, ferry crossing, o transfer bilang isang trip leg. Si Tara Gala na ang bahala sa pag-compute ng distance, travel time, estimated arrival, at travel expenses mo.

It's a simple, single-file web app (`index.html`) with no build step, no backend, and no account needed. **Lahat ng trip data mo, nasa browser mo lang.**

## ✨ Features: Ano'ng meron?

### 🚙 Planuhin ang biyahe

- **Trip legs:** I-record bawat drive, ferry crossing, o major transfer. Lagyan ng travel date, departure time, starting point, at destination.
- **Name your adventure:** Palitan ang trip title diretso sa page header. New trips start with **"San Tayo?"** — pangalanan ang gala mo kapag ready ka na. Mawawala ang prompt once you've renamed it.
- **Smart start time:** Kapag nag-add ka ng bagong trip leg, automatic na gagamitin ang arrival date at time ng previous leg bilang starting date at time. Less manual input, less hassle! Puwede mo pa rin itong baguhin anytime.
- **Route itinerary:** Automatic na naka-sort ang trip legs ayon sa date at departure time. Makikita mo ang distance, duration, estimated arrival, at cost ng bawat leg.
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
- **Expense breakdown:** Makikita mo kung magkano at ilang porsiyento ang share ng bawat expense category sa total trip budget.

### 📦 Lahat ng data, nasa iyo

- **Settings page:** Manage your trip data at Google Maps connection in one place.
- **Export to CSV:** I-download ang itinerary at expenses para madaling buksan sa spreadsheets.
- **Backup and restore:** I-save ang buong trip as a JSON file. Automatic na ginagamit ang trip title sa filename (halimbawa: `Gala-nelos-Overland-Trip-2026-backup.json`). Puwede mo ring i-restore sa ibang device o browser.
- **Local storage:** Nasa browser mo lang ang trip data. Walang account, walang backend, at walang ina-upload na trip information.

### 🌙 Simple lang, pero sulit

- **Dark theme:** Low-glare dark interface para mas comfortable sa mata.
- **Responsive layout:** Works on desktop, tablet, at mobile.
- **Mobile-friendly itinerary:** Sa phone, cards ang display ng itinerary at bottom sheets naman ang forms para mas madaling gamitin.

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
3. I-restrict ang API key sa required APIs at sa website address mo. Example: `https://your-username.github.io/*`.
4. Sa app, pumunta sa **Settings → Google Maps**, i-paste ang API key, at click **Save key**.

**Important:** Naka-store ang key sa browser mo. Hindi ito inilalagay sa source code o repository. Pero dahil client-side ang Google Maps integration, visible pa rin ang key sa browser environment. Make sure na naka-enable ang API restrictions at website referrer restrictions.

Ang keys na restricted sa website address ay hindi gagana kapag diretsong binuksan ang `index.html` mula sa computer mo. Gumamit ng hosted page or local server.

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
- **Backup your data:** Nasa browser local storage ang trip data. Kapag nag-clear ka ng site data, mabubura rin ito. Regular na mag-click ng **Save backup**.
- **Current location:** Kailangan ng secure HTTPS connection para ma-access ng browser ang location mo. Kaya mas reliable ang **Use my location** sa GitHub Pages kaysa sa locally opened file.
- **Google Maps billing:** May charges ang Google Maps services depende sa usage. I-check ang latest pricing at free usage limits ng Google Cloud account mo.

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
| **2.7.0** | **Smart Start Time:** New trip legs automatically start at the previous leg's arrival date and time. The starting date and time remain editable. |
| **2.6.1** | Roomier itinerary table: values stay on one line except Route. Wider page, with the expenses panel below the table on screens narrower than 1440 px. |
| **2.6.0** | Backup and CSV filenames follow the trip title. App version displayed in the footer and Settings. |
| **2.5.2** | The default title "San Tayo?" stays until the user names the trip. Any name is accepted. |
| **2.5.0** | New default title "San Tayo?" with a "Your next adventure" label and naming prompt. |
| **2.4.0** | Tara Gala browser tab icon. |
| **2.3.0** | Start trip in Google Maps from the leg form and itinerary. |
| **2.2.0** | Added the "Road Trip & Overlanding Planner" tagline and overlanding rig logo. |
| **2.1.0** | Fuel price and km/L carry over from the previous trip leg. |
| **2.0.0** | Tara Gala branding, editable trip title, Settings page, map pin picker, total distance, automatic fuel estimate, and itinerary icon buttons. |
| **1.2.0** | Use my current location as the starting point. |
| **1.1.0** | Google Maps place suggestions, automatic travel time, and estimated arrival. |
| **1.0.0** | Dark, responsive redesign and code cleanup. |

### Versioning guide

Every update gets a new version number:

- **Patch (`x.y.1`)** — Bug fixes and small improvements.
- **Minor (`x.1.0`)** — New features and functionality.
- **Major (`2.0.0`)** — Major redesigns or significant changes.

Remember to update `APP_VERSION` near the top of the script in `index.html` and add a new row to the version history.

---

## ❤️ Tara na!

Planuhin ang biyahe. Bantayan ang gastos. Sulitin ang bawat gala.

**Less hassle sa planning, more time sa adventure!**

**Tara Gala — Bawat biyahe, may kuwento.** 🇵🇭
