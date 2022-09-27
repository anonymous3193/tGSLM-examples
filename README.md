# Generative Spoken Language Model based on continuous word-sized audio tokens

## Abstract

We introduce a Generative Spoken Language Model based on continuous-valued audio tokens. 
We show that it is possible to replace the standard input of LM as abstract discrete types (one hot vectors) by continuous word-sized acoustic tokens, and still generate diverse and expressive language output. This is obtained by replacing table lookup for lexical types with a Lexical Embedding function, the cross entropy loss by a contrastive loss and multinomial sampling by k-NN sampling.  
The resulting model is the first generative language model based on continuous tokens. Its performance is on par with discrete unit GSLMs in terms of generation quality and zero resource challenge metrics. Moreover, it is 5 times more memory efficient because of its larger 200ms-long units. In addition, the token's embeddings before and after the Lexical Embedder are interpretable phonetically and semantically.

## Example generations

We provides some examples of our 200ms-tGSLM model. For comparison, we also provide example generations from GSLM (Lakhotia et al 2021). The reader may also refer to [the official website](https://speechbot.github.io/gslm/index.html)

For sampling, we chose the temperature parameter so that 200ms-tGSLM and GSLM generate batches of prediction with VERT score of the LJ corpus (VERT=0.189). We also sampled batches at the VERT of the Librispeech corpus (VERT=0.113). Samples are not conditionned on a speech prompt. Batches are composed of 100 sentences of 30 words each.

Audio examples are accessible in this github folders:

- 200ms-tGSLM@LJ-VERT: samples from a batch of generations at VERT=0.189
- 200ms-tGSLM@LS-VERT: samples from a batch of generations at VERT=0.113
- GSLM@LJ-VERT: samples from a batch of generations at VERT=0.189
- GSLM@LS-VERT: samples from a batch of generations at VERT=0.113
