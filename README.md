# AMI-diarization-setup

Diarization setup for AMI corpus[1] based on [Full-corpus-ASR partition](http://groups.inf.ed.ac.uk/ami/corpus/datasets.shtml). The diarization references are directly derived from the manual annotations, [version 1.6.2](http://groups.inf.ed.ac.uk/ami/download/). To generate the references:
- All words are considered as speech and included in the references. 
- Speaker turns respect precisely the annotations, but adjacent speech segments (words) of the same speaker are merged not to create false break points. Consecutive speech segments from the same speaker separated by pauses (silence) are not merged in any case.
Some researchers might find useful a version of diarization references that not only includes words but also vocal sounds as marked in the manual annotations and for this reason we also share such set of references. However, there are inconsistencies in what annotators marked as vocal sounds and we prefer the setup containing only words.

The uem files consider the whole lengths of the recordings.

[1] J. Carletta, S. Ashby, S. Bourban, M. Flynn, M. Guillemot, T. Hain, J. Kadlec, V. Karaiskos, W. Kraaij, M. Kronenthal, et al., The AMI meeting corpus: A pre-announcement, in: International workshop on machine learning for multimodal interaction, Springer, 2006, pp. 28–39.


### Scoring
For the sake of keeping this repository as simple as possible, we do not include scoring scripts. However, you can refer to the following links for examples on how to score using this setup [with dscore](https://github.com/BUTSpeechFIT/VBx/blob/35e7954ac0042ea445dcec657130e2c3c0b94ee0/AMI_run.sh#L64) or [with md-eval](https://github.com/kaldi-asr/kaldi/blob/d136b18346bee14166b950029405314401fc4a8b/egs/ami/s5c/run.sh#L138).
In order to use this setup directly with [pyannote](https://github.com/pyannote), refer to [this fork](https://github.com/pyannote/AMI-diarization-setup).


### Citations
In case of using the setup, please cite:\
F. Landini, J. Profant, M. Diez, L. Burget: [Bayesian HMM clustering of x-vector sequences (VBx) in speaker diarization: theory, implementation and analysis on standard tasks](https://arxiv.org/abs/2012.14952)


## Contact
If you have any comment or question, please contact landini@fit.vutbr.cz or mireia@fit.vutbr.cz