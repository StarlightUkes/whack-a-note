WHACK-A-NOTE — PWA HOSTING NOTES

Upload every file and folder in this package to the same HTTPS web directory:

  index.html
  manifest.webmanifest
  service-worker.js
  icons/

Important:
1. The site must be served over HTTPS. Service workers do not install from ordinary HTTP,
   except on localhost during testing.
2. Do not rename or separate the files unless you also update their relative paths.
3. Open index.html through a web server. Opening it directly as a local file will run the
   trainer, but installation and offline caching will not work.
4. On Android/Chrome, the Install App panel should appear when the browser confirms the
   page is installable.
5. On iPhone/iPad, open the page in Safari, tap Share, and choose Add to Home Screen.
6. A Zenler HTML lesson may run the trainer, but a PWA is most reliable when hosted at its
   own HTTPS URL where the service worker can control the app's directory.


IPHONE AUDIO UPDATE
-------------------
This version requests the iOS playback audio-session type and explicitly
unlocks Web Audio from the Start-button gesture.

To update an existing GitHub Pages deployment:
1. Replace index.html and service-worker.js in the repository.
2. Commit the changes.
3. Wait for the Pages deployment to finish.
4. On an iPhone that installed the old version, remove the old Home Screen app,
   visit the website again in Safari, and add it to the Home Screen again.
