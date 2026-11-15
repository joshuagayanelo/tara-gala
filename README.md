🇵🇭 Tara Gala!

Walang iwanan, puro gala lang! 🏕️🚙

Planning your next road trip or overlanding adventure? Tara, biyahe tayo!

Tara Gala is your Filipino-inspired Road Trip & Overlanding Planner. Whether you're cruising along highways, exploring mountain trails, or hopping between islands via RORO, we've got your trip planning covered.

Plan your routes, bantayan ang gastos, estimate your fuel, organize your RORO crossings, and keep your entire adventure in one place.

Less hassle sa planning, more time sa gala!

Built for Filipino road trippers, campers, overlanders, and families who love exploring the Philippines. 🇵🇭

✨ Features: Ano'ng meron?

🚙 Planuhin ang biyahe

- Trip legs: I-log bawat drive, ferry crossing, or major transfer. Add a route name, date, departure time, starting point, and destination.
- Route names: Lagyan ng highlighted label bawat leg (halimbawa, "Manila to Baguio") para madaling makita ang ruta sa itinerary.
- Editable trip title: Pangalanan ang adventure mo right from the page header. New trips start as "San Tayo?" with a prompt to give your gala a name. Mawawala ang prompt once you rename it.
- Smart defaults: Automatic na ang starting point ng bagong leg based sa previous destination. Pati date and time, naka-set sa estimated arrival ng previous leg. Editable pa rin lahat!
- No lost work: Kapag nag-click outside the leg form or nag-press ng Esc, tatanungin ka kung gusto mong i-save or i-discard ang changes.
- Route itinerary: Organized ang legs by date and departure time. Makikita mo ang distance, duration, estimated arrival, and expenses. Kung may accommodation note, kasama rin ang check-in and check-out details.
- Completed legs: Mark a leg as complete kapag natapos na ang biyahe. Lilipat ito sa collapsible Completed legs section. Puwede mong i-restore anytime using Mark as incomplete, or i-undo agad pagkatapos mag-complete.
- View mode: Click a row or tap a card, or use the eye icon, para makita ang complete leg details in read-only mode. Choose Edit or close kapag tapos ka na. On phones and tablets, full-screen ang view.
- Floating Add leg button: Hindi mo na kailangang bumalik sa taas! The Add leg button stays at the bottom right habang nag-i-scroll ka sa itinerary.
- Trip summary line: Makikita sa header ang date range, total days, and number of legs. Example: "Dec 14 to Dec 19, 2026 (6 days) • 6 legs planned".
- Trip summary: Quick overview ng total expenses, distance, travel time, and number of legs. Isang tingin lang, alam mo na ang progress ng gala!

🗺️ Hanapin ang ruta, let's go!

Powered by Google Maps integration, kapag nag-connect ka ng API key.

- Place suggestions: Search your starting point and destination with autocomplete. Philippines ang default search coverage.
- Pick on map: Search for a place, use your current location, or drop and drag a pin on the map. Hindi mo na kailangang hulaan ang exact place name!
- Use my location: Gamitin ang current location ng device mo as your starting point.
- Automatic distance and travel time: Automatically fills in the estimated distance (km) and driving time based on your selected places. Puwede mo pa ring i-edit manually.
- Estimated arrival: Automatic na kino-compute ang arrival time based on departure date, time, and travel duration. Kasama rin ang trips na tumatawid ng midnight.
- Start trip in Google Maps: One click lang para buksan ang route sa Google Maps, whether from the leg form or itinerary. Sa phone, puwede itong mag-launch ng turn-by-turn navigation.

💸 Bantay gastos!

Para hindi puro gala ang iniisip, pati budget bantayan natin!

- Automatic fuel estimate: Computes fuel cost using distance ÷ vehicle consumption (km/L) × fuel price per liter.
- Inherited fuel values: Fuel price and vehicle consumption carry over from the previous leg unless you change them.
- Expenses: Track fuel, food and dining, accommodation, RORO ferry and terminal fees, and miscellaneous expenses.
- Accommodation: I-record kung saan kayo mag-stay—campsite, hotel, or resort. Add check-in and check-out times alongside the accommodation price.
- Expense breakdown: Makikita mo kung magkano ang share ng bawat category sa total trip budget.

📦 Lahat ng data, nasa iyo

- Settings page: Manage your trip data and Google Maps connection in one place.
- Export to CSV: Download your itinerary and expenses para madaling buksan sa spreadsheets.
- Backup and restore: Save your entire trip as a JSON backup, named after your trip title. Example: "Gala-nelos-Overland-Trip-2026-backup.json". Puwede mo itong i-restore sa ibang device or browser.
- Local storage: Nasa browser mo lang ang trip data. Walang automatic uploads, account, or backend.

🌙 Simple lang, pero sulit

- Dark and light modes: Low-glare dark interface ang default. Switch to light mode anytime through Settings.
- Color combinations: Choose from five additional color combinations for each mode, or reset to the default colors.
- Responsive layout: Works on desktop, tablet, and mobile. Sa phones, cards ang itinerary and bottom sheets ang forms para mas madaling gamitin.

🚀 Paano magsimula?

Madali lang! No installation, no complicated setup.

1. Open "index.html" using your browser, or host it through GitHub Pages.
2. Click Add trip leg and fill in your route details.
3. Optional: Connect Google Maps para sa place suggestions, map pins, and automatic distance and travel time.

Walang Google Maps API key? No problem!

The app still works. You can manually enter places, distance, and travel time.

🗺️ Google Maps setup

Gusto mo ng autocomplete, map picker, current-location names, and automatic distance? You'll need a Google Maps API key.

Step 1: Create an API key

1. Visit "Google Cloud Console" (https://console.cloud.google.com/).
2. Create a project.
3. Create an API key.

Step 2: Enable the required APIs

Enable these APIs in your Google Cloud project:

- Maps JavaScript API
- Places API (New)
- Routes API
- Geocoding API (optional, for displaying pinned and current locations as addresses)

Step 3: Secure your API key

Before using the key:

- Set Application restrictions → Websites and add your website domain. For example: "https://your-username.github.io/*".
- Set API restrictions → Restrict key and allow only the APIs your app needs.
- Monitor API usage and billing. Set quotas and billing alerts where available.

Remember: A browser-based Google Maps API key is visible to visitors who inspect the page or network requests. It is not a secret, even if stored in browser storage. Website and API restrictions help protect it from unauthorized use.

Step 4: Connect it to Tara Gala

1. Open the app.
2. Go to Settings → Google Maps.
3. Paste your API key.
4. Click Save key.

The key is stored in your browser and is not written into your code or repository.

<text>Important: Keys restricted to a website address will not work when opening "index.html" directly using "file://". Use GitHub Pages or a local web server instead. For local testing, add the appropriate localhost website address to your key's website restrictions.</text>

The current app architecture does not require a backend. If you later add server-side Google Maps web-service calls, review the security setup and use an appropriate backend proxy and private credentials for those server-side requests.

🌐 Deploy with GitHub Pages

Gusto mong ma-access ang Tara Gala anywhere? Host it for free using GitHub Pages!

Step 1: Upload your file

1. Create a GitHub repository.
2. Upload "index.html" to the repository root.
3. Make sure the file is on the "main" branch.

Step 2: Enable GitHub Pages

1. Open your repository.
2. Go to Settings → Pages.
3. Under Build and deployment, select Deploy from a branch.
4. Choose "main" and "/ (root)".
5. Save your settings.

Step 3: Open your app

After a minute or two, your app should be available at:

"https://<your-username>.github.io/<repository-name>/"

That's it! Your own road trip planner is now online. 🚙

⚠️ Bago bumiyahe, tandaan!

A few reminders para smooth ang adventure:

- RORO travel time: Google's driving estimate may not include ferry crossings, terminal waiting time, boarding, or rest stops. Add the extra time manually to your travel duration.
- Back up your data: Trip information is saved in your browser's local storage. Clearing browser site data will delete it, so use Save backup regularly.
- Location access: Browsers require a secure HTTPS page to share your location. Use my location works on GitHub Pages but may not work when opening a local file.
- Google Maps billing: Google Maps services may incur charges. Check the latest pricing and free usage limits for your account.
- API key security: Restrict your browser key to your website and the APIs you actually use. Monitor usage regularly.

🛠️ Built with

Simple, lightweight, and walang komplikadong setup!

- HTML5 – App structure
- CSS3 – Styling and responsive layouts
- Vanilla JavaScript – App logic and interactions
- Google Maps JavaScript API – Optional Maps, Places, Routes, and Geocoding integration

No frameworks. No build process. No backend. No database.

Just one "index.html" file. Easy to run, easy to host, and easy to bring along sa next adventure!

📌 Version history

The current version is shown in the app footer and on the Settings page.

Version| Changes
3.5.2| Departure times in the itinerary use the 12-hour format (for example 10:00 PM). Arrival and check-in/out times use capital AM/PM too.
3.5.1| Smoother completed-leg flow: cards slide away, the rest of the page glides into place, the Completed legs panel eases open and closed, and its rows rise in one by one.
3.5.0| Mark trip legs as complete. Completed legs move into a collapsible "Completed legs" section where they can be viewed, restored (marked as incomplete) or deleted. Undo after marking.
3.4.0| The map picker now has a place search box and a My location button, in addition to tapping or dragging the pin.
3.3.0| Smooth open and close motion for the leg view and all other dialogs. On phones and tablets the leg view slides up like a sheet, and its sections fade in one after another.
3.2.1| Removed the blue tap flash on mobile. Cards and buttons still open and respond to taps.
3.2.0| Tap or click an itinerary row or card to open the leg view. The leg view fills the screen in card view. The Add leg button floats at the bottom right while scrolling. Smooth transitions on all buttons.
3.1.0| "Estimated costs" renamed to "Expenses". Food & dining, RORO ferry & terminal and Miscellaneous amounts are shown in the itinerary (₱0 in the table, hidden on cards when empty). Cards now take over from the table at 1400 px and below, and the expenses panel sits below the itinerary.
3.0.3| The leg number is shown at the top of each itinerary card on tablets and phones.
3.0.2| Route name placeholder changed to "e.g. Manila to Baguio".
3.0.1| The "Staying at" strip is hidden in the itinerary for legs with no accommodation note.
3.0.0| Route names, read-only view mode for legs, accommodation check-in and check-out, starting point inherits the previous destination, save-or-discard prompt on the leg form, durations shown as hrs and mins, trip summary with total days, staying-at strip in the itinerary, and Settings with dark/light mode and extra color combinations.
2.8.0| Accommodation notes: record where you are staying for each leg (for example "Dencels Hotel"). Shown in the itinerary and included in the CSV export.
2.7.0| A new trip leg starts on the previous leg's arrival date and time by default. It can still be changed.
2.6.1| Roomier itinerary table: every value stays on one line except Route. Wider page, and the expenses panel sits below the table on screens narrower than 1440 px.
2.6.0| Backup and CSV file names follow the trip title. App version shown in the footer and Settings.
2.5.2| The default title "San Tayo?" shows until the user names the trip. Any name, including "Gala-nelos Overland Trip 2026", is accepted.
2.5.0| New default title "San Tayo?" with a "Your next adventure" label and a naming prompt.
2.4.0| Tara Gala browser tab icon.
2.3.0| Start trip in Google Maps from the leg form and the itinerary.
2.2.0| Tagline "Road Trip & Overlanding Planner" and an overlanding rig logo.
2.1.0| Fuel price and km/L carry over from the previous trip leg.
2.0.0| Tara Gala branding, editable trip title, Settings page, map pin picker, total distance, automatic fuel estimate, icon buttons in the itinerary.
1.2.0| Use my current location for the starting point.
1.1.0| Google Maps place suggestions, automatic travel time and estimated arrival.
1.0.0| Dark, responsive redesign and code cleanup.

🔢 Versioning

Every update deserves a version number!

- Patch (x.y.1): Bug fixes and minor improvements.
- Minor (x.1.0): New features and functionality.
- Major (2.0.0): Big redesigns or significant changes.

When releasing an update:

1. Update "APP_VERSION" near the top of the script in "index.html".
2. Add the new version and its changes to the version history above.

Keep the version history updated para madaling ma-track ang improvements ng Tara Gala!

❤️ Tara na!

Planuhin ang biyahe. Bantayan ang gastos. Sulitin ang bawat gala.

Made with ❤️ for Filipino road trippers, campers, overlanders, and adventure-loving families.

Tara Gala! Bawat biyahe, may kuwento. 🇵🇭🏕️
