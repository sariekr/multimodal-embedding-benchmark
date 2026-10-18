# Multimodal Embedding Benchmark

AIMultiple evaluation of seven CLIP, SigLIP and ColPali models on image-text retrieval. The study uses MS-COCO for retrieval and Winoground for matching captions that describe different relationships between the same objects.

> [Read the benchmark on AIMultiple](https://aimultiple.com/multimodal-embeddings)

## Evaluation setup

- MS-COCO Karpathy test split with 5,000 images and 25,000 captions.
- Text-to-image and image-to-text retrieval, measured with Recall@1, @5 and @10.
- Winoground caption-image matching as a separate compositional reasoning task.
- A single NVIDIA A40 GPU for the reported measurements.

## Retrieval accuracy

Apple DFN5B-H achieves 50.1% text-to-image Recall@1. LAION CLIP-H reaches 46.3%, and OpenAI CLIP-L reaches 34.4%. Recall@1 counts a hit when the correct image ranks first.

Image-to-text retrieval accepts any of five captions for each image. Text-to-image retrieval has one correct image per caption. This difference affects the scores and limits direct comparisons between retrieval directions.

The article reports all seven models, retrieval results and the Winoground evaluation.

## Ownership

The benchmark implementation was developed for AIMultiple and belongs to AIMultiple. This repository contains a documentation summary. Source code and benchmark datasets are not distributed here.
