---
# Le poids est le numéro de la phase ; au-delà de nbPhases (hugo.toml), c'est le bilan.
title: "{{ replace (replaceRE `^\d+-` "" .File.ContentBaseName) "-" " " | strings.FirstUpper }}"
date: {{ .Date }}
weight: 0
summary: ""
images: ["couverture.jpg"]
cover:
  image: "couverture.jpg"
  alt: ""
  hiddenInSingle: true
  relative: true
draft: true
---

{{"{{<"}} frise titre="" {{">}}"}}

{{"{{<"}} fiche titre="La phase en bref" {{">}}"}}
| | |
|---|---|
| **Période** | |
{{"{{<"}} /fiche {{">}}"}}

## Première question ?

{{"{{<"}} conseils {{">}}"}}
- **Conseil** : explication.
{{"{{<"}} /conseils {{">}}"}}
