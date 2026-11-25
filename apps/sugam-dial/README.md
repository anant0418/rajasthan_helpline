# Sugam Dial

A small website that works like an app on your phone: call RSRDC offices for the Rajasthan districts
you pick, and keep complaints (with photos) and notes about them. Everything you save stays on your phone.

Material Design 2 look (Notes design system, Kumbh Sans).

## Install on the phone

1. Open the site's link in **Chrome** on the phone.
2. Tap **⋮ → Add to Home screen** (or **Install app**).
3. Open it from the home-screen icon. After the first visit it works without internet.

## What it does

Laid out like a contacts app: search on top, a side menu (a drawer on phones), one card of people.

- **First launch:** pick your districts. Change them from **Districts +** in the menu.
- **Contact list:** round initials, name, phone, post, district. Starred people first, then by rank
  (Top officers, DGM, Project Directors, Electrical/QC/Expressway, head office staff, yours).
  The menu picks whose contacts you see (Contacts, My districts, a district); chips filter them by
  post: All, Top officers, DGM, Project Directors, Electrical & QC, Head office.
  On a computer, Star and Edit appear only on the row under the mouse. Press **/** to search.
- **Person page:** numbers (tap to call), post and district, Star and Edit. **Complaints and notes**
  for that person: type a note and press Enter, start with **!** to log a complaint, or use
  **Complaint with photos**. On phones: round Call, Note and Complaint buttons.
- **Edit:** change a number ("edited" in the list, **Use the RSRDC number** to undo). Contacts you
  add can be renamed or removed.
- **Complaints page:** write one at the top (first line is the title), add photos from the camera
  or gallery, pick the district and office. Open / Resolved, comments, Share (WhatsApp, email,
  with photos), Mark resolved, Delete with Undo.
- **Notes page**, and after a call the app offers **Add note**.
- **Back up data / Restore backup** in the menu: one file with everything, photos included.

## Where data is kept

Browser storage on the phone: `localStorage` for text, IndexedDB for photos (shrunk to 1600 px JPEG).
Nothing is uploaded. Clearing Chrome's site data for this site deletes it, so back up now and then.

## Contact data

Contacts come from the **RSRDC telephone list as on 01-09-2026** (Rajasthan State Road Development &
Construction Corpn., pwd.rajasthan.gov.in/rsrdc → Contact directory, PDF). They live in `CONTACTS` in
`index.html`:

- **Project Directors** for each district they cover (Kekri is listed under Bhilwara, Karauli also
  covers Dholpur), with mobile numbers.
- **DGM groups**: each PD's DGM as printed in the list ("DGM- I" is read as DGM-I Jaipur, "DGM-II" as
  DGM-II Jaipur). The DGM shows up in every district of their group, and Search can add a whole group.
- **Electrical, QC and Expressway** PDs and the **Jaipur head office** (0141 3506 + extension,
  EPABX 0141 2708717, toll free 1800 891 4171), under Jaipur.

Office numbers the PDF prints incompletely (a lone STD code, or a number without one) are left out;
only mobiles are kept for those. Anyone can correct a number on their phone with the pencil
("Updated by you"), or add contacts of their own. Districts not in the list start empty.

## Files

```
index.html             the whole app (HTML, CSS, JS)
manifest.webmanifest   install name and icons
sw.js                  offline cache (bump VERSION when files change)
icon.svg, icon-maskable.svg
```
