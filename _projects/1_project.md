---
layout: page
title: Adaptive Optimal Rank Selection for KV Cache Compression
description: Soft-thresholded low-rank KV cache compression with custom Triton kernels for faster LLM generation.
importance: 1
category: Research
---

This project compresses the KV cache by selecting the rank of key and value projections through soft thresholding. The method achieves 4x compression with minimal loss, and reaches 20x compression when combined with low-rank-aware mixed-precision quantization.

With custom Triton-based GPU kernels, the system achieves 6.9x attention speedup and 3.1x end-to-end generation throughput improvement compared with PyTorch SDPA. This work appears in ICML as a spotlight paper.
