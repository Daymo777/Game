# William's Alphabet Game 🌈

A bright preschool typing game that teaches the QWERTY keyboard, made for a 3-year-old.

**To play:** just open `index.html` in any browser — no install, no internet needed. Works with a real keyboard, or by tapping the big on-screen keys on a tablet.

> This folder holds two games: the alphabet game in `index.html`, and **[🍉 Fruit Run](#-fruit-run)** in `fruit-game.html` — a platform dash for bigger kids, documented at the bottom of this file.

## How it works

A big colourful letter appears with an emoji friend ("A is for 🍎 Apple!") and the game says it out loud. William finds that letter on the keyboard and presses it — stars, confetti and cheers follow. There are no wrong answers: a missed key just wiggles, and the correct key starts bouncing in yellow as a hint.

## Levels

| Level | Challenge | Timer |
|-------|-----------|-------|
| 🐣 Learn | Letters A → Z in order, hint always shown | None |
| 🐢 Turtle | Random letters | 10 seconds |
| 🐰 Bunny | Random letters | 7 seconds |
| 🚀 Rocket | Random letters | 4 seconds |
| 🌈 Words | Spell whole words (CAT, SUN, MOON…) letter by letter | 8 seconds per letter |
| 💛 My Family | Type the names of the people William loves | 12 seconds per letter |
| 🔷 Shapes | Spell shape names (CIRCLE, STAR, ZIGZAG…) | 10 seconds per letter |
| 🔢 Numbers | Count the objects, then press the matching number key | 9 seconds |

The Numbers level reveals a real number row above the QWERTY keys — count the emojis (three balloons → press 3), with ten needing 1 then 0 just like a real keyboard.

If the timer runs out, nothing bad happens — the game just points out the key and waits. Ten stars finish a level with a big fanfare.

## Stopwatch and personal bests 🏆

A stopwatch in the header times each run from first letter to last star. When a level is finished:

- the win screen shows the run time,
- beating (or setting) the fastest time for that level triggers a **NEW PERSONAL BEST!** banner with extra fireworks,
- each level button on the menu shows its current best time.

Bests are saved on the device (localStorage), so they survive closing the browser. Capital-letter and small-letter modes keep separate bests.

## Sticker book 📖

Every finished level earns one random sticker into William's sticker book — 30 to collect across three sets: **Dinosaurs** 🦖, **Animals** 🦁 and **Mythical Monsters** 🐉. The book lives behind the 📖 button on the level menu; unfound stickers show as dashed "?" circles.

## Small letters mode 🔡

The **Letters: ABC / abc** toggle on the menu switches every level to lowercase, including the on-screen keyboard, so tablet play matches the letters in his books. On a physical keyboard the keys still show capitals, which quietly teaches the capital-to-small mapping. The choice is remembered between visits.

## Grown-ups' corner 🎙️

The 🎙️ button opens a recording screen where parents can record four short cheers in their own voice (correct letter, finished word, finished level, new personal best). Recordings stop automatically after 4 seconds, save on the device, and play instead of the robot voice. Recording needs microphone permission, so it works best with the game opened directly on the family tablet or phone.

To edit the family name list, change the `FAMILY` array near the top of the script in `index.html`.

## Notes for grown-ups

- Sound uses the browser's built-in voice (speech synthesis) and gentle chimes — no external assets, everything is in the single `index.html` file.
- Tested on desktop Chrome; touch input works for tablets.
- Motion is reduced automatically if the device has "reduce motion" switched on.

---

# 🍉 Fruit Run

A second, separate game lives in this folder: **`fruit-game.html`**. Open it in any browser — again no install, no internet, everything in the one file. It's aimed at older players than the alphabet game.

**The aim:** you start as a tiny blueberry on a very long platform. Reach the finish line 2,200 m away — and get there as the biggest fruit you can.

## How it works

You run forwards on your own; all you do is steer, jump and choose.

- **Match to grow.** Fruits lying on the platform that are *the same as you* glow with a yellow ring. Collect enough of them (2–6, more as you get bigger) and you ripen into the next fruit up. Wrong-sized fruits give a few points and a "too big!" / "too small!" — they don't count towards ripening.
- **Stay on the platform.** The deck narrows, and holes open up down the middle or along one edge. Roll off and the run is over.
- **Dodge the kitchen.** 🔪 knives (some sweep side to side), 🍴 forks, 🌀 blenders and chopping 🪓 cleavers knock you down a size. 🥖 rolling pins and 🧊 ice cubes are low enough to jump. 🍌 banana peels don't hurt, they just take your steering away for a moment.
- **Pick your gate.** Gates come in pairs across the platform and you must go through one of them. Green is kind, red is not.

| Gate | Effect |
|------|--------|
| ⬆️ RIPEN +1 / ⏫ RIPEN +2 | Grow a size (or two) on the spot |
| ✨ ×2 MATCH | Every matched fruit counts double for 14 s |
| 🛡️ SHIELD | Absorbs the next hit |
| 🧲 MAGNET | Matching fruits drift towards you |
| 🐌 SLOW-MO | Slows the run down for 7 s |
| ⭐ +500 | Straight points |
| 🔪 SLICED / 🪰 ROTTEN / 🥤 SQUEEZE | Down a size |
| ⚡ RUSH | Everything speeds up for 8 s |

### The fruit ladder

🫐 → 🍒 → 🍓 → 🍇 → 🥝 → 🍋 → 🍊 → 🍎 → 🍍 → 🍈 → 🍉

Getting knocked down a size is the usual cost of a hit, so being big is also your health bar. As the smallest fruit you get one bruise 🤕 for free — the next hit ends the run, until you ripen again.

### The three stretches

| Stretch | Feel |
|---------|------|
| 🌳 Orchard Walk | Gentle: wide deck, plenty of fruit, time to grow |
| 🔪 Kitchen Counter | Narrower, with knives, cleavers and blenders |
| 🏭 Juice Factory | Fast and mean — and the finish line |

## Controls

| | Keyboard | Touch |
|---|---|---|
| Steer | ← → or A / D | ◀ ▶ buttons, or drag anywhere |
| Jump | Space (or ↑ / W) | ⤴ button, or tap the screen |
| Pause | P or Esc | — |
| Start / restart | Enter or Space | the big button |

## Notes for grown-ups

- Your best score is saved on the device (localStorage) and shown on the title screen.
- The track is generated fresh every run, so no two runs are the same.
- Sound is a handful of WebAudio blips — no external assets. Screen shake and particles switch off if the device has "reduce motion" set.
- All the tuning lives in plain constants near the top of the script in `fruit-game.html`: `TRACK_LEN`, `BASE_SPEED` / `MAX_SPEED`, the `TIERS` ladder, `OBSTACLES` and `GATES`.
