# Slovníček – CZ–EN Vocabulary Trainer

A flashcard app for learning English vocabulary. It ships with ready-made sets for software documentation and ISTQB testing terminology, shows IPA pronunciation with audio, and moves words step by step from "don't know" to "know". You can add your own topic areas, and new terms are filled in automatically with their meaning and pronunciation.

**▶ Try it online:** https://sonkuc.github.io/slovnicek/

> The app's user interface is in Czech. It is built for Czech speakers learning English.

## Features

- **Flip cards:** the term on the front; the translation and pronunciation on the back. Click a card to flip it.
- **Two-way practice:** English → Czech and Czech → English.
- **Review mode (*Opakovat – Umím*):** check that you still remember words you already know. One correct answer in each direction is enough; a wrong answer moves the word back to *Neumím* ("I don't know").
- **Learning from scratch (*Od nuly*):** practise a small set of unknown words at a time (10–30, 20 by default). Each time you learn a word, a new one from the chosen area joins the set. Every new round starts with different words, and the app warns you before you leave a round in progress.
- **Progress tracking:** mark each answer ✓ or ✗. A word moves to *Umím* ("I know") after two correct answers in a row in each direction. A wrong answer resets its progress.
- **Topic areas:** create, rename, reorder and delete your own areas. Move words between areas, one at a time or in bulk.
- **Built-in vocabulary:**
  - *Softwarová dokumentace* (Software documentation): 180 terms such as API, deployment and deprecated
  - *ISTQB – testování* (ISTQB testing): 194 terms from the ISTQB CTFL v4.0.1 syllabus and the official CTFL v4.0 sample exams (A–D), excluding terms already in the previous set
  - *Obecná angličtina* (General English): an empty area for your own words
- **Smart word entry:** type an English term to get its IPA pronunciation and a Czech translation, or type only the Czech meaning to get the English equivalent and its pronunciation. All suggestions can be edited.
- **Duplicate detection:** you get a warning while typing if a term already exists, including variant spellings ("Black-Box Testing" vs. "black-box testing") and singular/plural forms.
- **Audio pronunciation:** played with the browser's built-in text-to-speech.
- **Backup and restore:** export all data to a `.json` file and import it again, for example on another device.
- **Light and dark mode**, with a responsive layout for desktop and mobile.
- **Keyboard shortcuts:** Space flips the card, ← = I know it, → = I don't know it.

## Getting started

- **Online:** open the link above. On a phone, use your browser's "Add to Home Screen" option to use it like an app.
- **Offline:** download `index.html` and open it in any modern browser (Chrome, Edge, Firefox). No installation is needed.

## Data storage and privacy

All words and progress are stored **only in your browser** (localStorage) and are never sent to a server. To move data between devices or keep a backup, go to **Oblasti → Stáhnout zálohu / Obnovit ze zálohy** (Areas → Download backup / Restore from backup).

> Note: clearing your browser's site data also deletes your vocabulary, so download a backup from time to time.

## Auto-fill

When you add a word, the app sends **only the term you typed** (English or Czech) to two free public services:

- [Free Dictionary API](https://dictionaryapi.dev/): IPA pronunciation and an English definition
- [MyMemory](https://mymemory.translated.net/): a suggested Czech translation, or an English equivalent when you start from Czech

Auto-fill needs an internet connection. Without one, you enter the translation and pronunciation manually.

## Tech stack

A single `index.html` file: HTML, CSS and vanilla JavaScript, with no frameworks, build step or backend. Pronunciation uses the Web Speech API.

## License

[MIT](LICENSE) © 2026 Sonkuc
