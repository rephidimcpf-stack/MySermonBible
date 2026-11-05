TELUGU BIBLE & SERMONS - installable app (PWA) package
======================================================

FILES
  index.html               the app (Bible + sermons + fonts embedded)
  manifest.webmanifest     app name, icon, full-screen settings
  sw.js                    service worker - makes it work offline after 1st load
  icon-192.png             app icon
  icon-512.png             app icon (large / maskable)
  apple-touch-icon.png     icon for iPhone/iPad home screen

STEP 1 - PUT THESE FILES ON A WEB ADDRESS (once, free, ~5 minutes)
  Option A - GitHub Pages
    1. Create a free account at github.com, then a new repository, e.g. telugu-bible.
    2. Upload all the files in THIS folder to the top level of the repository.
    3. Repository Settings -> Pages -> Source: "Deploy from a branch",
       Branch: main, Folder: / (root) -> Save.
    4. After a minute your app is at
         https://<your-username>.github.io/telugu-bible/

  Option B - Netlify Drop
    1. Go to app.netlify.com/drop and sign in (free).
    2. Drag this whole folder onto the page. You get a URL like
         https://telugu-bible-xyz.netlify.app

  Option C - Cloudflare Pages
    1. dash.cloudflare.com -> Workers & Pages -> Create -> Pages -> Upload assets.
    2. Upload this folder, deploy, note the URL.

  Any static host works. All files must sit at the same level (index.html at the root).

STEP 2 - INSTALL IT AS AN APP
  Android (Chrome): open the URL -> menu (3 dots) -> "Install app"
                    or "Add to Home screen". It gets a real icon and opens
                    full screen with no address bar.
  Windows (Chrome or Edge): open the URL -> the install icon in the address bar
                    (a small screen-with-arrow), or menu -> "Install Telugu Bible".
                    It appears in the Start menu and can be pinned to the taskbar.
  iPhone/iPad (Safari): Share -> "Add to Home Screen".

STEP 3 - GO OFFLINE
  Open the installed app once while online and let it finish loading (it caches
  the whole app, about 17 MB). After that it works with no internet at all -
  airplane mode included. Nothing else is ever downloaded.

UPDATING LATER
  Replace index.html on the host, and bump the version string in sw.js
  (change  var CACHE = 'telugu-bible-v1';  to v2). Then open the app once online.

NOTES
  - Sermons and settings are stored inside the app on each device. They do NOT
    sync between your phone and your PC. Use Settings -> backup (.json) and
    Import to move them across.
  - The voice reader uses the device's own speech engine. On Android install
    Google Text-to-Speech and download the Telugu voice
    (Settings -> System -> Languages -> Text-to-speech output -> Telugu).
  - If you host it, the page is public unless you use a private/unlisted URL.
    There is no personal data in it, only the Bible text.
