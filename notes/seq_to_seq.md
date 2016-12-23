## Sequence to Sequence Learning with Neural Networks

This paper presents a general end-to-end approach to sequence learning that makes minimal assumptions on the sequence structure

#### key points

* Uses two LSTM, one for encoding input, other one for decoding
* Can produce variable length output regardless of input length
* Uses beam search decoder to find probable output in reasonable time
* Providing input backward works better because start of the input is closer to start of the output

#### thoughts

* Breaking constraint that output length has to be same as input length is an amazing achievement
* Though at the beginning of decoding phase, network has to remember all aspects of input and I think this is a weakness

