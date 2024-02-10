Returned [[Lemma]] are sometimes incorrect, usually at the end stem. For example:
- anschleichen -> anschleich
- törichten -> törichn
- beglaubige -> beglaubig
## Possible Solutions
### Spacy Stanza
Possibly has better parsing for lemmas.
- Was not installing due to wheel error with most recent Python, so reverted to using Py37, which seems to have worked.
- Lemmatisation requires the entire context of the sentence at the very least to be effective. Currently the lemmatiser function is only being fed the word. This needs to be changed to include the entire context.