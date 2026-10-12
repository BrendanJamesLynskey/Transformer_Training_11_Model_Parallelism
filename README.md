# Transformer Training 11 — Model Parallelism: Pipeline, Tensor, Sequence and Expert

When one device cannot hold the model, cut it up: layer by layer (a pipeline, with its bubble), inside each layer (tensor parallelism), along the sequence, or among experts. A live pipeline simulation, 3-D and 4-D layouts, and a systems model checked against published runs.

**Live site:** https://brendanjameslynskey.github.io/Transformer_Training_11_Model_Parallelism/

Pipeline parallelism and the bubble (live GPipe/1F1B simulation); interleaving; tensor parallelism's column/row splits; sequence, context and expert parallelism; 3-D/4-D layouts; the systems model against 12 published runs.

## Live, animated companion

This deck is the slide companion to Part 2 (Training) of [Transformer Decoder Explained](https://transformer-decoder-explained.vercel.app/training), where the same model trains in your browser:

- [Chapter 12: Parallelism II: model](https://transformer-decoder-explained.vercel.app/training/12-model-parallelism)

## Where the numbers come from

Every measured number on these slides comes from the site's [results.md](https://github.com/BrendanJamesLynskey/transformer-explainer/blob/main/results.md) (seeded NumPy reference runs; CI recomputes them), filled in at build time from its `results.json`. Numbers from papers are cited on the slide with a link. The model is tiny (5,376 parameters, one book, a CPU): its runs show mechanisms, not what happens at scale, and the slides say so where it matters. GPU runs of the site's Colab notebooks are pending; no GPU number appears here.

Part of the [Transformer Training sub-hub](https://github.com/BrendanJamesLynskey/LLM_Hub_Transformer_Training) &middot; [LLMs hub](https://github.com/BrendanJamesLynskey/LLMs)
