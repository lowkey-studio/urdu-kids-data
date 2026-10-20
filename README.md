# Urdu for kids: open data

Small, hand-checked data for anyone building Urdu learning material for children: the 38 letters with their joined forms, picture words, Urdu numbers 1 to 100, word pairs, short graded stories and two public-domain poems, each in Urdu, Roman Urdu and English.

These files power [Takhti](https://takhti.appin60.com), a free printable Urdu worksheet maker (playgroup to grade 3).

| File | What it holds |
|---|---|
| `letters.json` | 38 letters in Urdu alphabet order, how each joins, every joined form as text (using U+200D ZERO WIDTH JOINER), and a picture word with Roman Urdu, English and an emoji |
| `numbers-1-100.json` | Urdu digit and number word for 1 to 100 (common spellings; a few vary between books) |
| `word-pairs.json` | Opposites, singular and plural, masculine and feminine, with Roman Urdu and English |
| `stories.json` | 12 short graded stories: each line in Urdu, Roman Urdu and English, five new words, two questions |
| `poems.json` | Allama Iqbal's "Lab pe aati hai dua" and "Hamdardi" (public domain) and the rhyme "Machhli jal ki rani hai", with translations |
| `names.json` | Common children's names, Roman spelling to Urdu |

## Joined forms in one line

```js
const ZWJ = "‍";
const start = letter + ZWJ, middle = ZWJ + letter + ZWJ, end = ZWJ + letter;
```

Letters that join only to the letter before them (ا د ڈ ذ ر ڑ ز ژ و ے) have no start or middle form. Render with an Urdu font such as [Noto Nastaliq Urdu](https://github.com/notofonts/nastaliq).

## Licence

Data, stories and translations: CC BY 4.0, credit "Takhti (takhti.appin60.com)". The Iqbal poem text is in the public domain.

Found a wrong form or spelling? Open an issue or email takhti@appin60.com.
