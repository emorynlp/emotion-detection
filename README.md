# Emotion Detection

Emotion Detection aims to classify a fine-grained emotion for each utterance in multiparty dialogue.
Our annotation is based on the primary emotions in the Feeling Wheel (Willcox, 1982).
We must admit that the inter-annotator agreement of this annotation is not the greatest; we welcome any contribution from the community to improve the annotation quality.
This task is a part of the [Character Mining](../../../character-mining) project led by the [Emory NLP](http://nlp.mathcs.emory.edu) research group.

<p align="center">
<img height="500" src="http://nlp.mathcs.emory.edu/character-mining/img/feeling-wheel.jpg">
</p>


## Dataset

Each utterance is annotated with one of the seven emotions, *sad*, *mad*, *scared*, *powerful*, *peaceful*, *joyful*, and *neutral*, that are the primary emotions in the Feeling Wheel.

* Latest release: [v1.0](https://github.com/emorynlp/emotion-detection/archive/emotion-detection-1.0.tar.gz).
* [Release notes](https://github.com/emorynlp/emotion-detection/releases).

## Statistics

The following episodes are used for the training, development, and evaluation sets:

* Train (TRN): [s01\_e02, s01\_e03, s01\_e04, s01\_e05, s01\_e06, s01\_e07, s01\_e08, s01\_e09, s01\_e11, s01\_e12, s01\_e13, s01\_e14, s01\_e16, s01\_e17, s01\_e18, s01\_e19, s01\_e21, s01\_e22, s01\_e23, s01\_e24, s02\_e01, s02\_e02, s02\_e03, s02\_e04, s02\_e05, s02\_e06, s02\_e07, s02\_e09, s02\_e11, s02\_e12, s02\_e13, s02\_e14, s02\_e15, s02\_e16, s02\_e17, s02\_e18, s02\_e19, s02\_e21, s02\_e22, s02\_e24, s03\_e02, s03\_e03, s03\_e04, s03\_e05, s03\_e06, s03\_e07, s03\_e10, s03\_e11, s03\_e12, s03\_e13, s03\_e14, s03\_e15, s03\_e16, s03\_e17, s03\_e18, s03\_e19, s03\_e22, s03\_e23, s03\_e24, s03\_e25, s04\_e03, s04\_e04, s04\_e05, s04\_e07, s04\_e08, s04\_e09, s04\_e11, s04\_e12, s04\_e13, s04\_e14, s04\_e15, s04\_e16, s04\_e18, s04\_e19, s04\_e22, s04\_e23, s04\_e24]
* Development (DEV): [s01\_e15, s01\_e20, s02\_e10, s02\_e20, s03\_e01, s03\_e09, s03\_e21, s04\_e01, s04\_e06, s04\_e10, s04\_e21]
* Evaluation (TST): [s01\_e01, s01\_e10, s02\_e08, s02\_e23, s03\_e08, s03\_e20, s04\_e02, s04\_e17, s04\_e20]

| Dataset | Episodes | Scenes | Utterances |
|:-------:|---------:|-------:|-----------:|
| TRN     | 77       | 713    | 9,934      |
| DEV     | 11       | 99     | 1,344      |
| TST     | 9        | 85     | 1,328      |
| Total   | 97       | 897    | 12,606     |

| Dataset | Neutral | Joyful | Peaceful | Powerful | Scared | Mad   | Sad |  Total |
|:-------:|--------:|-------:|---------:|---------:|-------:|------:|----:|-------:|
| TRN     | 3,034   | 2,184  | 900      | 784      | 1,285  | 1,076 | 671 | 9,934  |
| DEV     | 393     | 289    | 132      | 134      | 178    | 143   | 75  | 1,344  |
| TST     | 349     | 282    | 159      | 145      | 182    | 113   | 98  | 1,328  |
| Total   | 3,776   | 2,755  | 1,191    | 1,063    | 1,645  | 1,332 | 844 | 12,606 |

## Annotation

Each utterance has the field `emotion`.
Three utterances in the following example are annotated with the emotions of *Neutral*, *Joyful*, and *Powerful*, respectively.

```json
{
  "utterance_id": "s01_e02_c01_u002",
  "speakers": ["Joey Tribbiani"],
  "transcript": "Yeah, right!.......Y'serious?",
  "tokens": [
    ["Yeah", ",", "right", "!"],
    ["......."],
    ["Y'serious", "?"]
  ],
  "emotion": "Neutral"
},
{
  "utterance_id": "s01_e02_c01_u003",
  "speakers": ["Phoebe Buffay"],
  "transcript": "Oh, yeah!",
  "tokens": [
    ["Oh", ",", "yeah", "!"]
  ],
  "emotion": "Joyful"
},
{
  "utterance_id": "s01_e02_c01_u004",
  "speakers": ["Rachel Green"],
  "transcript": "Everything you need to know is in that first kiss.",
  "tokens": [
    ["Everything", "you", "need", "to", "know", "is", "in", "that", "first", "kiss", "."]
  ],
  "emotion": "Powerful"
}
```

## Citation

* [Emotion Detection on TV Show Transcripts with Sequence-based Convolutional Neural Networks](https://arxiv.org/abs/1708.04299). Sayyed Zahiri and Jinho D. Choi. In The AAAI Workshop on Affective Content Analysis, AFFCON'18, 2018.


## Contact

* [Jinho D. Choi](http://www.mathcs.emory.edu/~choi).
