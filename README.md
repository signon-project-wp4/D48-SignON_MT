# D48-SignON_MT

This repository implements the SignON_MT class, which enables the translation between spoken and sign languages represented by glosses.


## Languages and models




This contribution is part of the SignON Project (https://signon-project.eu)

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
