# How to use in `pyannote`


```python
# tell pyannote.database where to find partition and reference
import os
os.environ["PYANNOTE_DATABASE_CONFIG"] = 'AMI-diarization-setup/pyannote/database.yml'

# initialize 'only_words' experimental protocol
from pyannote.database import get_protocol
only_words = get_protocol('AMI.SpeakerDiarization.only_words')

# iterate over the training set
for file in only_words.train():
    meeting = file['uri']
    reference = file['annotation']

# iterate over the development set
for file in only_words.development():
    pass

# iterate over the test set
for file in only_words.test():
    pass

# initialize 'word_and_vocalsounds' experimental protocol
word_and_vocalsounds = get_protocol('AMI.SpeakerDiarization.word_and_vocalsounds')
```
