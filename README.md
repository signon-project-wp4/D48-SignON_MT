# D48-SignON_MT

This repository implements the SignON_MT class, which enables the translation between spoken and sign languages represented by glosses. This contribution is part of the SignON Project (https://signon-project.eu) and, namely, is the implementation of the different approaches and models reported in the deliverable _"Deliverable 4.8: Final Routines for transformation of text from and to InterL"_

## Languages and models

It includes models for Spanish Sign Language (LSE), German Sign Language (DGS), British Sign Language (BSL) and The Netherlands Sign Language (NGT) and it also implements a multilingual model. The models were trained using SLs corpora and the two learning approaches reported in  _"Deliverable 4.8: Final Routines for transformation of text from and to InterL"_.

| Language | Approach 1 link | Approach 2 link |
| ------------- | ------------- | ------------- |
| LSE | 2.4.1 | 2.4.1 |
| BSL | 4.19.2 | 2.4.1 |
| NGT | 1.19.5 |  2.4.1 |
| SDGS | [LINK](https://github.com/google/sentencepiece) |


## Requirements
This research was developed using Python 3.8.0. Below, the library requirements are listed to assure the experiments reproducibility.

| Resource | Version/URL |
| ------------- | ------------- |
| Tensorflow | 2.4.1 |
| Transformers | 4.19.2 |
| Numpy | 1.19.5 |
| SentencePiece | [LINK](https://github.com/google/sentencepiece) |

## Example of usage
```python
model = SignON_MT(7)
spoken_input = 'tiefer luftdruck bestimmt in den nÃ¤chsten tagen unser wetter'
gloss_input = 'DRUCK TIEF KOMMEN'

encoded_sentence = model.encode(gloss_input.lower(), 'DGS')
decoded_sentence = model.decode(encoded_sentence, 'de_DE')
print(decoded_sentence)
```
#### Output:
    der tiefdruck zieht weiter nach norddeutschland
