# Sugam Dial

A small website that works like an app on your phone: call PWD offices in the Rajasthan districts you
pick, and keep complaints (with photos) and notes about them. Everything you save stays on your phone.

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
- **Bottom tabs:** Districts, Complaints (Open / Resolved, across all districts), Notes.
- **Backup:** **⋮ → Back up data** saves one file with everything, photos included. Keep it on
  WhatsApp or Drive. **⋮ → Restore backup** brings it back on a new phone.

## Where data is kept

Browser storage on the phone: `localStorage` for text, IndexedDB for photos (shrunk to 1600 px JPEG).
Nothing is uploaded. Clearing Chrome's site data for this site deletes it, so back up now and then.

## Office data

The office list is **sample data** (structure only, no phone numbers) until the Sugampath directory is
loaded. Districts are the 41 districts of Rajasthan. To load the real list, edit `SAMPLE` in
`index.html` (each row: district, circle, has circle office, divisions, sub-divisions) and add
`phone` values, or replace it with the full Sugampath export.

## Files

```
index.html             the whole app (HTML, CSS, JS)
manifest.webmanifest   install name and icons
sw.js                  offline cache (bump VERSION when files change)
icon.svg, icon-maskable.svg
```
