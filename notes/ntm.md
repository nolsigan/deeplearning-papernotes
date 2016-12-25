## Neural Turing Machines

Extended capabilites of neural networks by coupling them to external memory resources. The combined system is analogous to a Truing Machine or Von Neumann architecture but is differentiable end-to-end.

#### key points

* NTM can infer simple algorithms such as copying, sorting, and associative recall from input and output examples! (WOW)
* NTM is a differentiable computer that can be trained by gradient descent
* Resembles working memory of human brain and uses addressing mechanism to choose what to read from memory
* Reading is defined as multiple of weight vector and memory info
* Writing is decomposed to erase followed by add
* Addressing is a combination of content-based and location-based
* NTM with LSTM controller works the best

#### thoughts

* Main achievement of this paper is using memory and addressing
    * I think to go toward general AI, location-based addressing has to be removed
    * But location of memory should be used like cache and start content-based addressing from near locations
* NTM with LSTM controller resembles Von Neumann architecture
    * wonder if brain works similar