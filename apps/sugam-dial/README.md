# Sugam Dial

A small website that works like an app on your phone: call RSRDC offices for the Rajasthan districts
you pick, and keep complaints (with photos) and notes about them. Everything you save stays on your phone.

Material Design 2 look (Notes design system, Kumbh Sans).

## Install on the phone

1. Open the site's link in **Chrome** on the phone.
2. Tap **⋮ → Add to Home screen** (or **Install app**).
3. Open it from the home-screen icon. After the first visit it works without internet.

## What it does

- **First launch:** pick your favourite districts. Change them later from **⋮ → Change districts**,
  or add a district or a whole circle from **Search**.
- **District page:** two tabs.
  - **Complaints:** write a complaint right at the top, attach photos from the camera or gallery,
    choose the whole district or one office, tap **Add**. Each complaint has comments, Share
    (WhatsApp, email, with photos), Mark resolved and Delete with Undo.
  - **Contacts:** grouped as Circle (SE), Divisions (XEN), Sub-divisions (AEN). Call button, and a
    pencil to update the number ("Updated by you", with **Use Sugampath number** to undo).
    **Add contact** for anyone not in the list.
- **Office page:** Call, Complaint, Note, the number, and that office's complaints and notes.
- **After a call:** coming back to the app offers **Add note**.
- **Bottom tabs:** Districts, Contacts (every contact in one list, search by name, post, district or
  number, **My districts** or **All**), Complaints (Open / Resolved, across all districts), Notes.
- **Backup:** **⋮ → Back up data** saves one file with everything, photos included. Keep it on
  WhatsApp or Drive. **⋮ → Restore backup** brings it back on a new phone.

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
