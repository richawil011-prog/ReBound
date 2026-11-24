Rebound
Twenty-two minutes. Then the basin lets go.
A first-person mystery set in a drowned city at the end of the world. Every twenty-two minutes the Rebound Engine pulls the whole basin back to the same moment, and only you remember. You don't get stronger. You learn: the schedule, the codes, the people, and what the Engine is really holding on to.
Made by NyxiePlaysGames. Runs in the browser with Three.js and the Web Audio API. No downloads, no accounts.
---
Play
On itch.io: open the game page and press Run game. Fullscreen is recommended.
Locally: see Run it yourself below.
Rebound is made for a keyboard and mouse, and also works with a controller. Headphones help.
Controls
Action	Keyboard and mouse	Controller
Move	`W` `A` `S` `D` or arrow keys	Left stick
Look	Mouse (click the game to capture it)	Right stick
Run	`Shift`	Left stick click or left trigger
Jump	`Space`	Bumpers
Interact, talk, continue	`E`	A
Wait (let time pass until the next thing you know about)	`T`	X
Journal	`J` or `Tab`	Y
Pause, back	`Esc`	Start, B
Hide the interface (for screenshots)	`H`	
Every key can be changed in Settings → Keys (click an action, press the key you want; a key already in use swaps over). The arrow keys always move as well.
Settings also include separate Music, Effects, Ambience and Voices volumes, plus brightness, mouse sensitivity, invert look, field of view, bloom, film grain, head bob, camera shake, subtitles, text size and subtitle size. Quality goes from High down to Lowest, which halves the resolution and turns off shadows, bloom and grain for older laptops; if the game runs slowly at the start it steps down on its own.
There is no timer on screen. Time in the basin keeps running while you read, talk or look at your journal; only the pause menu stops it. Tell the time from the bell tower, the sky, and the basin itself.
Saving
Progress saves automatically in your browser (localStorage): your journal, everything you have solved, and which cycle you are on. New journey on the title screen wipes it.
---
What's in it
Halcyon Station. A round habitat on a mast with the Rebound Engine turning in its domed hall, the berths where you wake, a radio room, a gallery that faces the sunset, and an archive sealed from the inside.
The Hollow City. The Sky Bridge, the Upper Terrace with a bell tower whose clock has twenty-two hours, the Concourse under four transit arches, the Civic Archive, Vale Court, the Market Pier, the old Service Walk, the transit span and South Plaza.
The Deep. A tidal intake with a lock, a run that floods with the tide, and a laboratory.
The Core. A pressure ring under the sea, and the light that stands over the basin.
Lantern Isle, Verdant Rise and the Tarn Rooftops. Reached by the skiff and its pilot, Luka.
Six residents who never got on the boats, each with a voice of their own, and a day of their own: at set times they walk off to the things they do every cycle (making up an empty bed, sorting the same apples, watering the bed they were told not to water, lighting the lamp at dusk) and mutter about it if you're close. They blink, breathe, and turn to look at you.
Keanu, a black German Shepherd asleep on the bed next to yours in berth 03. Give him a belly rub and he'll follow you round the station. Somewhere in the station is a book that will help you understand him, and once you do, he'll point you towards whatever you're stuck on. His ball is lying by the writing desk: pick it up, look at him and throw it, and he'll bring it back.
Little secret books. How to Speak Dog, How to Speak Robot and How to Speak Fish are lying about the basin. Each one changes a conversation, and the journal's Curiosities page keeps track of the small secrets you've found (with a nudge towards the ones you haven't).
Six letters the residents wrote to each other on the night of the boats (Skye and Absol, Christian and Charley, Aiden and Luka), hidden around the basin with the reader's name on each envelope.
Life around the basin. Gulls over the water and on the pier bollards (walk up to one and it takes off), fish that leap near the piers, butterflies in the glasshouse, fireflies on Lantern Isle in the evening, dust turning in the light of the Civic Archive.
A visitor. At the bottom of the long stairs into the Deep, Milky, a white-furred explorer, is mapping the tunnels with a notebook and a ball of string. Tell them what you find and they go further each cycle; if you met them, they make the boat at the end.
Memories. The ending changes with what you found and who you helped: letters, a tomato, a flask, a ball, Milky's map, an apple bought at last, a fish let go, one last look. Each version you've seen is kept on the journal's Memories page, even across new games.
Quiet spots. A bench on the Upper Terrace, the end of the Market Pier, the gallery window in the station, the corner of the deck on Verdant Rise: sit down and watch for a while. Each one is a Curiosity.
Fishing. Charley's spare rod leans on the pier rail. Cast off the south side, wait for the float to dip, and reel in. You might catch an old boot, a tin of peaches, a note in a bottle, or the same fish as yesterday.
Weather. Some cycles a fog rolls in before dawn and burns off by eight; some cycles a shower comes through in the early afternoon, everything outside goes dark and glossy with puddles, and the residents have something to say about it. Shelter under Skye's awning if you like.
Residents meet up. Skye walks out to Charley on the pier in the afternoon; Christian and Aiden talk on the radio; last thing at night, Absol calls Skye.
Small kindnesses. Skye's awning comes loose every cycle; a tomato from the Rise or a cup of tea from the berths kettle can go a long way (residents' prompts change to Give… when you're carrying something for them). Each one is a Curiosity, and finding one now pops up a quiet note.
Notices pinned up: in the station corridor the tide warning, a hand-drawn map of the basin, the kettle rota (two names crossed out), lights out and the skiff; in the Deep laboratory, the intake tide chart.
An ending you watch: the beam goes up, the basin reaches morning, the residents gather on the Market Pier, and Luka takes everyone out into the sunrise (Keanu in the bow), trading flashes with the lighthouse on the way.
A schedule. Lanterns flare at 03:00, the intake drains at 06:00, light crosses the gallery at 08:00, towers fall, the span fails at 15:00, the relay wakes at 18:30, the grid dies at 20:00, and at 22:00 everything sinks.
A journal. Questions, notes taped in as you find them, the schedule as you learn it, the people you've met, and a map drawn from memory. It goes through every rebound with you: notes yellow, crease, collect coffee rings and tear, and in the last minutes of a cycle the water comes up the page.
Run it yourself
The game is static files, but browsers don't load ES modules from `file://`, so serve the folder:
```bash
node serve.mjs          # http://127.0.0.1:8080
# or
python3 -m http.server 8080
```
Upload to itch.io
Zip the contents of this folder so that `index.html` is at the top level of the zip.
On itch.io, create a project, set Kind of project to HTML, and upload the zip.
Tick This file will be played in the browser.
Set the viewport to 1280 x 720, and enable Fullscreen button and Click to launch in fullscreen if you like.
Save, then view the page and play it once from start to the first rebound.
Project layout
```
index.html            entry point
css/style.css         the interface
fonts/                Rebound Hand, the hand lettering (built by tools/build\_hand\_font.py)
vendor/               three.js r170 (MIT)
js/main.js            boot, plus a small test handle (window.\_\_rb)
js/core/              renderer and post-processing, geometry batching, collision
js/world/             materials, sky and sea, station, city, deep and core, isles, people, props
js/game/              game loop, story data, the schedule, puzzles, save state
js/ui/                HUD, panels, dialog, journal, menus, settings
js/audio/             synthesised sound, ambience and the generative score
docs/                 art bible, development notes, checklist, walkthrough (spoilers)
```
Everything you see and hear is generated in code: no image, model or audio files. Even the lettering is pen strokes: the interface font is built from them, and every sign in the basin is painted, stencilled, carved or chalked from them and then weathered.
Credits
Game design and story: made by NyxiePlaysGames
World, levels and artwork: made by NyxiePlaysGames
Music and sound: made by NyxiePlaysGames
Writing: made by NyxiePlaysGames
Programming: made by NyxiePlaysGames
Keanu: himself, a very good boy
Milky: a cameo, down in the Deep
Built with three.js (MIT) and the Web Audio API
Lettering: drawn by hand for Rebound, stroke by stroke (js/ui/hand.js)
License
The game's code is MIT licensed; see `LICENSE`. three.js and the fonts keep their own licenses in `vendor/` and `fonts/`.
