# Magic New Year 2027 Gala Dinner – table reservations

Springfield @ Sea · 31 Dec 2026. Interactive floor plan, reservation form, summary, guest register and admin-only table setup.

* `index.html` – the whole app (floor plan image included). No guest data is stored in this file.
* `firebase-config.js` – Firebase project id + web API key (these only identify the project; access is controlled by the rules).
* `firestore.rules` – paste into Firebase → Firestore → Rules. Only the listed staff email can read/write.

Bookings are kept in Google Firestore (collections `gala2027_bookings`, `gala2027_config`), so every signed-in staff device sees the same data (refreshes every 10 s).
Staff sign in with the shared staff email + password created in Firebase → Authentication. Table Setup also needs the admin PIN.
Use Table Setup → Backup & import to export or restore everything.
