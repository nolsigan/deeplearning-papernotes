## Connectionist Temporal Classification: Labelling unsegmented Sequence Data with RNN

This paper presents a novel method called CTC for training RNNs to label unsegmented sequences directly, thereby solving pre-segmenting, post-processing problem.

#### key points

* This paper classifies two ways for labelling data sequences, temporal classification(TC) and framewise classification(FC)
    * TC takes unsegmented data sequences as whole and provides whole labelling
    * FC provides independent labelling for each data frame
* Uses RNN for TC and call it 'connectionist temporal classification'(CTC)
* RNN tries to minimize number of insertions, substitutions and deletions required to change output to correct labels
* Decodes output paths to find most probable answer
    * Best path decoding : find most probable labelling - fast but less accurate
    * Prefix search decoding : modifies forward-backward algorithm, efficiently calculate

#### thoughts

* I reached this paper from other modern text recognition papers - seems like a promising way to deal with unsegmented sequences directly
* Published in 2006, results are way lower than state-of-the-art papers but shown that deep learning exceeds old methods like HMM
