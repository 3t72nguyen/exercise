# Military Calisthenics: install on iPhone

## Option A: add to Home Screen (no Mac, no Apple developer account)
1. Put the contents of the `web` folder on any HTTPS web host. Free options: Netlify Drop (app.netlify.com/drop), Cloudflare Pages, GitHub Pages. Drag the `web` folder in and you get a URL.
2. Open that URL in **Safari** on your iPhone (it must be Safari).
3. Tap **Share**, then **Add to Home Screen**, then **Add**.
4. Open it from the new icon. It runs full screen and works offline after the first load.

Voice counting and sounds start after your first tap on a button (an iPhone rule). Keep the phone's silent switch off for sound.

## Option B: native app with Xcode (needs a Mac)
1. Install Xcode and Node.js on the Mac.
2. In this folder run:
   - `npm install`
   - `npx cap add ios`
   - `npx cap sync ios`
   - `npx cap open ios`
3. In Xcode choose your iPhone, set a Team under Signing & Capabilities (a free Apple ID works), change the bundle id `com.example.militarycalisthenics` to your own, then press Run.
4. Replace the default app icon with `icon-1024.png` in Assets.

A free Apple ID build expires after 7 days and must be re-installed. A paid Apple Developer account ($99/year) lets you use TestFlight or the App Store.
