# Instructions for AI assistants

If you're asked to create Anki flashcards or a deck from this repository:

1. Read `FLASHCARD_GUIDE.md` in full first and follow it.
2. Check `backup/exports/all_notes.md` so you don't duplicate existing cards.
3. Use the note types listed in `backup/settings/note_types.json` where possible.
4. Deliver the deck in one of the formats in section 9 of the guide.
5. **Save every deck you create in its own repository** under the GitHub organization `prsnlanki`, cloned into `~/organizations/prsnlanki/<deck>` and named in the deck's own language, lowercase ASCII (`deutsch`, `espanol`). Copy the layout of an existing deck repo ([prsnlanki/deutsch](https://github.com/prsnlanki/deutsch)): a `build.py` that packages its subdeck folders into one `.apkg` (git-ignored, published as a versioned GitHub Release with `scripts/publish.sh`), the source data, a `README.md` for the deck and each subdeck, a `CHANGELOG.md`, `.local-ci`, and Psittacus as the submodule `psittacus/` when the deck has audio. That repo's `CLAUDE.md` has the rules for changing it. A new kind of card for an existing deck is a new subdeck folder in that deck's repo, not a new deck.
   Name the deck and its subdecks in Anki in the deck's own language, for immersion (`Languages::Deutsch::Verben`, `Languages::Español::01 Refranes`), and make the README's title that name.
   Then add the deck to the "Decks" table in this repository's `README.md`, commit and push.
6. When you update an existing deck, keep note GUIDs stable so re-importing updates cards instead of duplicating them.

## Repository layout

- Decks are not here: each has its own repository (see rule 5 above and the Decks table in `README.md`).
- `addons/` — add-ons the owner develops, each linked as a git submodule to its own repository. Never copy an add-on's source in here; to add a new one, run `git submodule add <repo-url> addons/<name>` and list it in `addons/README.md`.
- `backup/` — a snapshot of the owner's local Anki: collection, settings, the configs of installed add-ons, and readable exports. Regenerate `settings/` and `exports/` with `backup/tools/regenerate.py`. Keep only the latest snapshot and overwrite it (git history keeps old versions). Never commit `prefs21.db` (it holds the AnkiWeb login) or media from third-party decks. Never copy add-on code into `backup/addons/`, only each add-on's `config.json` and `meta.json`; record every installed add-on (name, version, source, AnkiWeb code if any) in the "Installed add-ons" table of `backup/README.md` rather than copying their code.
