SmartTask PWA update
====================

Upload these files to the ROOT of the same Cloudflare Workers static-assets deployment:
- index-rota.html (rename this file to index.html when deploying)
- manifest.webmanifest
- sw.js
- icons/icon-192.png
- icons/icon-512.png

Keep the folder structure exactly as shown. The HTML expects /manifest.webmanifest,
the service worker at /sw.js, and the icons under /icons/.

After deployment on HTTPS:
1. Open the site in Chrome on Android.
2. Refresh the site.
3. Chrome menu (three dots) > Install app / Add to Home screen.
4. If an old icon is cached, remove the old home-screen shortcut, clear site storage/cache,
   reopen the site, then install it again.

Important:
- This package updates the front-end HTML and PWA assets.
- Supabase database/RLS/RPC policies are server-side and are not changed by an HTML upload.
  Confirm backend permissions separately before using real company data.
