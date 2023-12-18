# Multi Party Coreference Resolution

## Overview
The project focuses on character identification in multiparty dialogues, specifically addressing the task of classifying characters in a TV show. Two tasks were considered: "Main + Others" and "All." The team decided to focus on the "All" task, aiming to classify all characters in the show, including the main characters and others. The complexity of this task lies in handling a large set of classes, leading to a unique approach for solving it.

## Baseline
The baseline model, AMORE-UPF, achieved success by combining an entity library with a Bi-LSTM model. The entity library enhances performance, demonstrating that even with relatively simple architectures, effective results can be obtained. The team plans to build upon this baseline by introducing modifications and attention-based mechanisms.

## Model Architecture
The AMORE-UPF baseline model consists of the following components:

1. **Embedding Layer:** Responsible for creating embeddings for entities and speakers, acting as the entity library.

2. **Bi-LSTM Layer:** Processes word and speaker embeddings to calculate the predicted speaker vector.

3. **Dense Layer:** Generates the predicted speaker vector from the Bi-LSTM's hidden state for each reference.

4. **Cosine Similarity and Softmax:** Compares the reference speaker vector with entities in the entity library, applying a softmax layer to cosine similarity values.

5. **Dropout Layers:** Two dropout layers after the tanh activation and after the Bi-LSTM layer.

The team aims to introduce a Transformer architecture to further improve the model's performance.

## Transformer Architecture
The proposed C2 framework utilizes a joint coreference resolution and character linking approach in multiparty conversation. It employs a pre-trained transformer text encoder and a mention-level self-attention module. The model contextualizes mentions using pre-trained language models and appends speaker embeddings to each mention. The Mention-Level Self-Attention layer refines mention representations, and coreference resolution and character linking are formulated as joint optimization tasks.


## Conclusion
The team is dedicated to enhancing the baseline model and exploring innovative solutions to address the challenges of character identification in multiparty dialogues. The inclusion of a Transformer architecture is expected to further improve model performance. Future work involves rigorous experimentation and fine-tuning to achieve optimal results.

## Team Members
- [Abhijeeth Singam](https://github.com/AbhiSingam)
- [Tushar Jain](https://github.com/tushar994)
- [Rishabh Khanna](https://github.com/RishKhanna/)
