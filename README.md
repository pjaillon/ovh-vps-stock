# OVHcloud VPS Stock Dashboard

A lightweight single-page dashboard that tracks live stock availability for OVHcloud VPS plans, including Local Zone coverage in North America and Europe.

## Features
- Merges availability data for all public "VPS 2025" plans.
- Supplements Local Zone inventory (NA `.LZ`, EU `.LZ-eu`) so those regions show real stock instead of placeholders.
- Interactive filters: select plans, search by datacenter code/name, toggle hiding empty rows, and collapse Local Zone sections.
- Dark/light theme toggle with system preference support and skeleton loading state.

## Usage
1. Open `OVHcloud_vps_stock.html` in any modern browser.
2. Wait a moment for the live OVHcloud API requests to finish; the timestamp updates when complete.
3. Use the filter bar to narrow the table:
   - Check/uncheck plans or use **All/None** shortcuts.
   - Type into "Search datacenter" to match codes or friendly names.
   - Toggle **Hide empty rows** to remove regions with no stock under current filters.
   - Expand/collapse the Local Zone sections as needed.
4. Click a plan chip to open the corresponding OVHcloud configurator link in a new tab.

## Notes
- The page relies on client-side fetches to the public OVHcloud API. Keep the browser console open if you need to watch for network failures or rate limiting warnings.
- Only a subset of plan suffixes (`.LZ`, `.LZ-eu`) currently expose Local Zone data; additional regions can be added by extending `LOCAL_ZONE_FETCH_CONFIG` in the script.
- No build step is required—commit updates directly to the HTML file.

## License
Released under the MIT License. See [`LICENSE`](LICENSE) if present, or choose an appropriate license for your deployment.
