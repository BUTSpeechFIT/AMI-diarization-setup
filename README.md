# AMI-diarization-setup

Diarization setup for AMI corpus[1] based on [Full-corpus-ASR partition](http://groups.inf.ed.ac.uk/ami/corpus/datasets.shtml). The diarization references are directly derived from the manual annotations, [version 1.6.2](http://groups.inf.ed.ac.uk/ami/download/). To generate the references:
- All words are considered as speech and included in the references. 
- Speaker turns respect precisely the annotations, but adjacent speech segments (words) of the same speaker are merged not to create false break points. Consecutive speech segments from the same speaker separated by pauses (silence) are not merged in any case.
Some researchers might find useful a version of diarization references that not only includes words but also vocal sounds as marked in the manual annotations and for this reason we also share such set of references. However, there are inconsistencies in what annotators marked as vocal sounds and we prefer the setup containing only words.

[1] J. Carletta, S. Ashby, S. Bourban, M. Flynn, M. Guillemot, T. Hain, J. Kadlec, V. Karaiskos, W. Kraaij, M. Kronenthal, et al., The AMI meeting corpus: A pre-announcement, in: International workshop on machine learning for multimodal interaction, Springer, 2006, pp. 28–39.

### pyannote

In order to avoid any future divergence between this repo and [`pyannote.audio`](https://www.github.com/pyannote/pyannote-audio) evaluation protocols, we also [provide](pyannote) the [`pyannote.database`](https://www.github.com/pyannote/pyannote-database) configuration file.

### Citations
In case of using the setup, please cite:\
F. Landini, J. Profant, M. Diez, L. Burget: [Bayesian HMM clustering of x-vector sequences (VBx) in speaker diarization: theory, implementation and analysis on standard tasks](https://arxiv.org/abs/2012.14952)


## Contact
If you have any comment or question, please contact landini@fit.vutbr.cz or mireia@fit.vutbr.cz