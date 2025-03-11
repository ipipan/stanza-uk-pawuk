# stanza-uk-pawuk

This repo contains resources necessary to load uk-pawuk Stanza models.

## Building a Pipeline
```
pipe = stanza.Pipeline(lang='uk-pawuk', resources_url="https://raw.githubusercontent.com/ipipan/stanza-uk-pawuk/main", resources_version="1.9.0")
```

## Example
```
text = "4 лютого почалася битва за Манілу."
doc = pipe(text)
print(doc)
```

```
[
  [
    {
      "id": 1,
      "text": "4",
      "lemma": "4",
      "upos": "ADJ",
      "xpos": "number",
      "feats": "Case=Gen|Gender=Neut|NumType=Ord|Number=Sing|Uninflect=Yes",
      "head": 3,
      "deprel": "obl",
      "start_char": 0,
      "end_char": 1
    },
    {
      "id": 2,
      "text": "лютого",
      "lemma": "лютий",
      "upos": "NOUN",
      "xpos": "noun:inanim:m:v_rod",
      "feats": "Animacy=Inan|Case=Gen|Gender=Masc|Number=Sing",
      "head": 1,
      "deprel": "nmod",
      "start_char": 2,
      "end_char": 8
    },
    {
      "id": 3,
      "text": "почалася",
      "lemma": "початися",
      "upos": "VERB",
      "xpos": "verb:rev:perf:past:f",
      "feats": "Aspect=Perf|Gender=Fem|Mood=Ind|Number=Sing|Tense=Past|VerbForm=Fin",
      "head": 0,
      "deprel": "root",
      "start_char": 9,
      "end_char": 17
    },
    {
      "id": 4,
      "text": "битва",
      "lemma": "битва",
      "upos": "NOUN",
      "xpos": "noun:inanim:f:v_naz",
      "feats": "Animacy=Inan|Case=Nom|Gender=Fem|Number=Sing",
      "head": 3,
      "deprel": "nsubj",
      "start_char": 18,
      "end_char": 23
    },
    {
      "id": 5,
      "text": "за",
      "lemma": "за",
      "upos": "ADP",
      "xpos": "prep",
      "feats": "Case=Acc",
      "head": 6,
      "deprel": "case",
      "start_char": 24,
      "end_char": 26
    },
    {
      "id": 6,
      "text": "Манілу.",
      "lemma": "Манілу.",
      "upos": "PROPN",
      "xpos": "noun:inanim:m:v_zna:prop:geo",
      "feats": "Animacy=Inan|Case=Acc|Gender=Masc|Number=Sing",
      "head": 4,
      "deprel": "nmod",
      "start_char": 27,
      "end_char": 34,
      "misc": "SpaceAfter=No"
    }
  ]
]

```