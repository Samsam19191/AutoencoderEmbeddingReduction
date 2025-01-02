# French-Reduced-Word-Embedding

This project explores the reduction and fine-tuning of high-dimensional word embeddings to achieve computational efficiency while preserving semantic integrity. Using FacebookAI's FastText embeddings as the baseline, we developed a pipeline to compress French word embeddings from 300 to 30 dimensions through AutoEncoder architectures and refined them with Word2Vec-based fine-tuning.

## Project Overview

### Objectives
1. **Compression**: Achieve a 10x reduction in the dimensionality of embeddings using AutoEncoder architectures.
2. **Fine-Tuning**: Enhance the semantic quality of compressed embeddings with a Word2Vec model trained on tailored Skip-gram pairs.
3. **Evaluation**: Validate the embeddings through metrics such as cosine similarity and visualization techniques.

### Methodology
- **AutoEncoder Design**: We experimented with a two-layer AutoEncoder, optimizing hyperparameters (e.g., hidden layer dimensions, learning rate, batch size) to balance reduction efficiency and semantic quality.
- **Data Engineering**: 
  - Processed a French Wikipedia corpus with SpaCy.
  - Generated Skip-gram word pairs for training, focusing on contextual integrity despite limitations in phrase segmentation.
- **Fine-Tuning**:
  - Employed a Word2Vec architecture to refine the reduced embeddings.
  - Tackled computational constraints by limiting vocabulary size and applying optimization techniques like early stopping and learning-rate scheduling.
- **Evaluation**:
  - Compared embeddings using cosine similarity for semantic closeness.
  - Applied PCA for visualizing cluster formations within the reduced embeddings.

### Results
1. **Reduction**: Achieved a promising 10x dimensionality reduction with the AutoEncoder while retaining a significant portion of semantic quality.
2. **Fine-Tuning**: Refined embeddings exhibited meaningful improvements in specific clusters but did not surpass the original 300-dimensional embeddings in overall complexity.
3. **Insights**: Smaller reduction factors (e.g., 5x) may provide better results with enhanced fine-tuning and computational resources.

### Observations
- Cluster visualizations highlighted the potential for capturing semantic relationships even in reduced dimensions, though some structural fidelity was lost.
- Limitations in training data size and hardware resources constrained the scope of fine-tuning and evaluation.

### Future Directions
- Explore smaller reduction ratios to balance dimensionality and performance.
- Increase training corpus size and computational capacity to fully realize the potential of fine-tuning.
- Expand evaluation to real-world NLP benchmarks for comprehensive validation.

This project demonstrates the feasibility of significant dimensionality reduction while retaining semantic information, offering a pathway to computationally efficient NLP solutions.
