# 神笔 Shénbǐ community library

Packs of extra words, poems, short books and reading practice for the Shénbǐ Chinese-learning game.
The game's **Community → Library** lists everything in `index.json` and downloads `packs/<id>.json`.

## Share a pack

1. In the game: **Community → Make packs → New pack**. Add words (things can get your own picture;
   without one they appear as an ink seal), poems, books and reading sentences.
2. **Try it in my game**, then **Save as file…**
3. Open a pull request that adds your file to `packs/`, or send the file to the library's keeper.
   (The keeper publishes with `python3 tools/publish_pack.py your-pack.json`, which checks the pack
   and updates `index.json`.)

Please only share what you made yourself or what may be shared (classical poems are fine; pictures
must be your own or free to use). Keep it friendly for learners of all ages.

## Pack format (version 1)

One JSON file: `id`, `version`, `title`, `title_zh`, `author`, `description`, and any of
`words`, `poems`, `books`, `sentences`, plus `images` (PNG/JPEG data URLs), `strokes` (stroke order,
hanzi-writer data) and `listen` (speech recognition data). The pack maker fills in pinyin, stroke
order and speech data by itself. See `shenbi/packs.py` in the game for the details.
