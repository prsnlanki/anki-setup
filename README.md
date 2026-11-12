# Anki setup

The hub of my Anki setup: links to the decks I make and the add-ons I build (each in its own repository under [prsnlanki](https://github.com/prsnlanki)), and a backup of my local Anki setup. Plus a master guide for making excellent flashcards.

**Asking an AI to make a deck?** Point it at this repository and tell it the subject. It should start with [`FLASHCARD_GUIDE.md`](FLASHCARD_GUIDE.md) and [`CLAUDE.md`](CLAUDE.md).

## Layout

| Folder | Contents |
|---|---|
| [`addons/`](addons/) | Add-ons I develop, linked to their own repositories |
| [`backup/`](backup/) | Snapshot of my local Anki: collection, settings, installed add-ons and readable exports |
| [`FLASHCARD_GUIDE.md`](FLASHCARD_GUIDE.md) | Evidence-based guide to writing ideal flashcards, for any subject |

## Decks

Each deck lives in its own repository, with its source data, build script and audio. Each deck and subdeck is named in its own language, for immersion. Every version stays on the deck's releases page; its `CHANGELOG.md` says what changed.

| Deck | Notes | Description |
|---|---|---|
| [English](https://github.com/prsnlanki/english) ([download 1.0.0](https://github.com/prsnlanki/english/releases/download/v1.0.0/English.apkg)) | 444 | **Expressions:** phrases, collocations and idioms by context: IELTS, work, emails, negotiating, emotions, friends and more, with audio |
| [Deutsch](https://github.com/prsnlanki/deutsch) (German, [download 2.0.0](https://github.com/prsnlanki/deutsch/releases/download/v2.0.0/Deutsch.apkg)) | 2,508 | **Verben** (1,994): the 2,000 most common German verbs by frequency: German definition, principal parts, gapped example sentence, a second meaning for 174 common verbs. **Ausdrücke** (514): Funktionsverbgefüge, verb + preposition + case, collocations, discussion, work/email phrases and idioms for B2→C1, in subdecks by type, with audio |
| [Español](https://github.com/prsnlanki/espanol) (Spanish, [download 2.0.0](https://github.com/prsnlanki/espanol/releases/download/v2.0.0/Espanol.apkg)) | 676 | For a native speaker, all in Spanish: **Refranes** (173) to complete, with German and English equivalents; **Locuciones** (151), **Colocaciones** (116) and **Vocabulario culto** (144) to produce from a definition and a gapped sentence; **Norma y dudas** (92) from the RAE's DPD. Panhispanic, regionalisms tagged, with audio |
| [Esperanto](https://github.com/prsnlanki/esperanto) ([download 2.1.0](https://github.com/prsnlanki/esperanto/releases/download/v2.1.0/Esperanto.apkg)) | 2,402 | For an intermediate speaker, all in Esperanto: **Verboj** (1,997), the 2,000 most common verbs by frequency; **Vortfarado** (90) to build words with affixes; **Vortprovizo** (9), precise words and false friends; **Korelativoj kaj partikloj** (44); **Gramatiko** (63) to choose the right form and learn the rule. **Esprimoj** (199): prepositions, collocations, linking words and set phrases, and proverbs from Zamenhof's *Proverbaro*. Audio by eSpeak NG |

## Add-ons

| Add-on | Description |
|---|---|
| [Ink](https://github.com/prsnlanki/ink) | Minimal, information-dense redesign of the deck list, overview, reviewer and stats page (formerly Anki Dashboard) |
| [Psittacus](https://github.com/prsnlanki/psittacus) | Replaces Anki's text-to-speech with modern neural voices |

## Cloning

`addons/` uses git submodules, so clone with:

```
git clone --recurse-submodules https://github.com/prsnlanki/anki-setup
```

In an existing clone, run `git submodule update --init` to fetch them.
