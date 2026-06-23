========================================================
KSP QUOTE & INVOICE APP — README (for David)
========================================================

WHAT THIS IS
------------
A simple, standalone web app (a PWA) for Kim Schafer Plastering.
Kim can:
  - take/upload a photo of a handwritten quote or invoice
  - type/correct the details
  - generate a professional KSP-branded PDF quote or invoice
  - keep a list of quotes, invoices and customers
  - export everything (PDFs + CSV summaries) for tax time

SEPARATE FROM EVERYTHING ELSE
-----------------------------
This project is completely independent. It does NOT connect to or touch:
GrassRoots Mowing Co, Project #156, Cherry, Granny Language Lessons, or any
existing Render service, GitHub repo, database, domain, or env variables.
  - GitHub repo to create:  ksp-quote-invoice-app
  - Render service name:    ksp-quote-invoice-app
  - Render type:            Static Site
  - Build command:          blank
  - Publish directory:      .  (repo root)  — see DEPLOY-TO-RENDER.txt

HOW DATA IS STORED  (IMPORTANT)
-------------------------------
There is no server database. All records (quotes, invoices, customers,
settings, and uploaded photos) are saved in the browser's local storage
ON THE DEVICE KIM USES.

What this means:
  - Records are tied to that phone + that browser.
  - Use the in-app "Export" button regularly to back everything up.
  - If Kim changes phones or browsers, EXPORT FIRST, because the new
    device starts empty.
  - If the browser data/cache is cleared, un-exported records are lost.
  - The app reminds Kim of this on the Dashboard and Export page.

KIM ONLY NEEDS THE LINK
-----------------------
Kim does NOT need GitHub, Render, folders, zips, commands, or developer
tools. You deploy once; you send her the Render link; she adds it to her
home screen. That's it.

WHAT'S IN THIS FOLDER
---------------------
  index.html           the whole app (PDF + zip libraries and the KSP logo
                       are embedded inside, so it works offline)
  manifest.json        PWA settings (name, colours, icons)
  service-worker.js    offline caching so the app opens without signal
  icons/               app icons made from the KSP logo
  DEPLOY-TO-RENDER.txt  step-by-step deployment guide
  README-FOR-DAVID.txt  this file

UPDATING LATER
--------------
  1. Edit the files.
  2. Commit/upload to the ksp-quote-invoice-app GitHub repo.
  3. Render auto-redeploys.
  4. Kim re-opens the app; it refreshes to the new version.

SUPPORT NOTES
-------------
  - Default business details (phone, email, bank, etc.) are pre-filled and
    can be changed in the app's Settings page.
  - Quote numbers: QT-2026-001, QT-2026-002 ...
  - Invoice numbers: INV-2026-001, INV-2026-002 ...
  - GST defaults to 10% and can be turned off in Settings.
