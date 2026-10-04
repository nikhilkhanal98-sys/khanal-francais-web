# Khanâl Français: web app

My French course, from zero to B2 in 36 weeks, as a web app. It's the same app as the Windows and Android versions.

There's no passcode: anyone with the link can open it. It's kept out of search engines, so people only find it if you share the link.

## What's inside

- `dist/` is the whole app: lessons, all 38,431 audio clips packed into 444 small bundles, and the offline service worker.
- `dist/_headers` keeps the site out of search results.

## Put it online with Cloudflare Pages (free)

1. In Cloudflare, go to **Workers & Pages**, then **Create**, then **Pages**, then **Connect to Git**, and pick this repository.
2. Build settings:
   - Framework preset: **None**
   - Build command: *(leave empty)*
   - Build output directory: **dist**
3. Click **Save and Deploy**.

## On a phone

Open the link.

- On iPhone, tap **Share**, then **Add to Home Screen**.
- On Android, tap the menu, then **Install app**.

The app then opens full screen, like a normal app.

## Limits of the web version

- The study alarm only rings while the app is open. For an alarm that rings with everything closed, use the Windows or Android app.
- Audio downloads as you use it, one lesson day at a time, and is then kept for offline use.
- AI chat voices use the recorded clips or your device's own French voice.

## Rebuilding after course changes

From the main project folder, run:

```
python tools/build-web.py
```

This writes a fresh `web/dist`. Then commit and push, and Cloudflare redeploys on its own.
