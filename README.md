# batch-effect-removal-for-cell-annotation

The goal of my project was to label the cells in a new dataset from [Delorey et al](https://www.nature.com/articles/s41586-021-03570-8.). using the categories from the [Human Lung Cell Atlas](https://github.com/LungCellAtlas/HLCA). However, the two datasets had a large batch effect, which made it hard for a simple classifier to work well. To overcome this challenge, I did the following:

- I used some preprocessing steps to normalize and scale the data
- I fine-tuned a pre-trained transformer model called [`Geneformer`](https://huggingface.co/ctheodoris/Geneformer) with the reference dataset
- I used the fine-tuned model to reduce the batch effect and enable the classifier to assign labels to the cells in the new dataset
