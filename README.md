# Richmo Pizzeria Manager

## Put it online (GitHub Pages)
Upload EVERYTHING inside this folder (index.html, sync.js, sync-config.js, config.js, supabase-setup.sql and the assets folder) to your repository, wait a minute, then press Ctrl+F5.
Starter PINs: Owner 1111, Reception 2222 (you can change them in Staff & settings).

## Make every device show the same data + audit log (Supabase)
1. Go to supabase.com, sign in, click New project (free plan is fine). Name it "richmo". Wait until it is ready.
2. Left menu: SQL Editor > New query. Open supabase-setup.sql from this folder, copy everything, paste, click Run.
3. Left menu: Project Settings > API Keys. Copy the Project URL and the Publishable key (starts with sb_publishable_). NEVER use the secret / service_role key.
4. Open sync-config.js in this folder and paste them:
   window.BB_SYNC = { url: "https://xxxx.supabase.co", key: "sb_publishable_...", row: "richmo" };
5. Upload sync-config.js to GitHub again. Open the site on the device that has your data FIRST, then open it on other devices.
6. A small "Synced" badge appears at the bottom right. Orders, tables, menu, stock and the Audit log are now shared. Every action is also stored in the audit_log table in Supabase.
Tip: use a NEW Supabase project for Richmo so it never mixes with Bun Bun.

## Printing
Choose the receipt printer in the print window, set Margins to None. Receipts are cut to the 80mm roll size.
