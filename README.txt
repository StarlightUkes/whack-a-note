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


INSTRUCTION TEXT UPDATE
-----------------------
The opening text now includes suggested ranges for low-G ukulele,
baritone ukulele, and bass.


TWO-MODE UPDATE
---------------
Root Mode:
- A new note appears on beat 1.
- Clicks sound on beats 1–3.
- The root sounds on beat 4.

Root–Fifth Mode:
- A new root appears on beat 1.
- Clicks sound on beats 1–2.
- The root sounds on beat 3.
- The fifth below (a perfect fourth below the displayed root) sounds on beat 4.


BASS-TONE UPDATE
----------------
The target tones now use a synthesized electric-bass-style pluck with a strong
fundamental, brief bright attack, low-pass decay, and upper harmonics that keep
very low notes audible on phone and tablet speakers.


ACOUSTIC-GUITAR UPDATE
----------------------
- Root Mode now defaults to G1–C3.
- Root–Fifth Mode now defaults to A1–C3.
- Changing modes automatically applies that mode's default range.
- Reference tones now use a brighter acoustic-guitar-style pluck with a
  short pick transient and rapidly decaying harmonics.


CLEAR-PITCH UPDATE
------------------
- Include sharps is unchecked by default.
- Include flats is unchecked by default.
- The reference sound is now a clean, sustained organ-style harmonic tone.
- Strong upper harmonics make low pitches easier to hear on small speakers.


MODE/HELP CORRECTION
--------------------
- Fixed the mode-specific instructions at the top of the app.
- Expanded How to Play to explain Root and Root–Fifth modes.
- Removed invalid extra markup and unused backup files.
- Updated the service-worker cache version.
