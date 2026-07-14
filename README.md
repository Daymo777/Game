# William's Alphabet Game 🌈

A bright preschool typing game that teaches the QWERTY keyboard, made for a 3-year-old.

**To play:** just open `index.html` in any browser — no install, no internet needed. Works with a real keyboard, or by tapping the big on-screen keys on a tablet.

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
