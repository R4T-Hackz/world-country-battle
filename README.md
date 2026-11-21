String Circle — World Country Battle
A tiny, fast battle game for your phone. Pick 2–5 countries, hit start, and watch
their balls bounce around a circular arena cutting each other's strings. The last
country with strings left wins.
No sign-up. No ads. No internet needed to play (flags look nicer with internet).
1. Install the app (Android)
Download: open the Releases page on the right side of this repository and
download StringCircle-WorldCountryBattle-1.0.0.apk.
Then:
1.
Tap the downloaded file (from the notification shade, or your Files/Downloads app).
2.
Android will say *"For your security, your phone is not allowed to install unknown
   apps from this source"* — this is normal for apps that do not come from the Play Store.
3.
Tap Settings → turn on Allow from this source → go back.
4.
Tap Install.
5.
If Play Protect shows a scan prompt, tap Install anyway (the app is open source
   and the code is right here in this repository).
6.
Tap Open and play.
Requirements: Android 5.0 (Lollipop) or newer. About 1 MB of space.
The APK is signed with a standard debug key, which is the normal way open-source
Android builds are shared outside the Play Store. That is why the warnings appear.
Cannot install?
Problem
Fix
"App not installed"
You may already have a different build installed. Uninstall the old one first.
"Blocked by Play Protect"
Tap More details → Install anyway.
No "Install unknown apps" option
Settings → Apps → Special app access → Install unknown apps → choose your browser/Files app → Allow.
Download stops on mobile data
The file is ~1 MB; try again on Wi-Fi or a different browser.
Nothing happens on tap
Open your Files app → Downloads → tap the .apk from there.
2. Play in the browser (no install)
Open index.html from this repository on any phone or laptop. It is one single file —
no server, no build step.
If the project has GitHub Pages turned on, the game also runs at
https://R4T-Hackz.github.io/world-country-battle/.
3. How to play
1.
Tap Countries (top-left) to open the setup screen.
2.
Choose how many countries are fighting: 2, 3, 4 or 5.
3.
For each slot, tap the country to search and pick any nation from 195 countries.
4.
Set strings per country with the slider — anywhere from 1 to 80 (default 50).
5.
Tap Start.
Then just watch. Balls bounce, collide and cut rival strings. A country is knocked out
the moment its last string is cut. The winner's flag and time appear on screen.
One round usually takes 25–45 seconds.
Want a different fight? Tap Random for a fresh set of countries, or Replay to
run the same one again.
4. Buttons
Button
What it does
Countries
Setup screen: number of countries, which country, how many strings
Start / Pause
Starts the battle, pauses and resumes it
↺ Restart
Runs the same battle again from zero
Random
Picks new random countries
1.0x
Speed of the simulation: 0.75x, 1.0x, 1.5x, 2.0x
Speaker
Mute or unmute the sound
Eye
Clean mode — hides all buttons so you can screen-record a clean battle
5. Tips
•
More strings = longer, more dramatic battles. 60–80 gives long duels; 15–25 is a
  quick, chaotic round.
•
5 countries is chaos — everyone cuts everyone. 2 countries is a clean 1v1 duel.
•
1.5x speed is the sweet spot for sharing clips; 0.75x makes the cuts easy to follow.
•
Use clean mode + screen recording to make a vertical video of a battle.
6. Questions
Does it need internet?
Only for flag pictures and fonts. Without internet the game still plays; flags fall back
to emoji.
Does it collect any data?
No. There is no analytics, no tracking, no ads, no account. The app only loads flag
images from flagcdn.com.
Is it the same as the browser version?
Yes — the app is a small wrapper that opens the exact same index.html file full-screen.
Where are my settings saved?
They are not saved. Every time you open the app you get the default setup (3 countries,
50 strings each). Use the Countries screen to change it.
Can I use it on iPhone?
Not as an APK. Open index.html in Safari and it works the same way.
Can I change the game?
Yes — it is one readable HTML file. SKILL.md explains where every setting lives
(gravity, speeds, colours, countries, sounds), and CHANGELOG.md lists what changed
in each version.
7. For developers
bash
# play it
open index.html

# build the APK (JDK 17 + Android SDK 34)
cp index.html android/app/src/main/assets/index.html
cd android && gradle assembleDebug
Pushing a tag like v1.0.1 makes GitHub Actions build the APK and attach it to a new
release automatically.
Path
What it is
index.html
The entire game
android/
WebView wrapper project
dist/
Prebuilt APK
SKILL.md
Full technical reference and tuning guide
CHANGELOG.md
Version history
8. Credits
Flags from flagcdn.com · Font: Inter ·
Styling: Tailwind CSS
Made for fun. Not affiliated with any country, government or flag authority — the flags
are just team colours.
