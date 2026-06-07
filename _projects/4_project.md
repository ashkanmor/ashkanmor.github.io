---
layout: page
title: Token-Adaptive Low-Rank KV Cache Compression
description: PIM-enabled low-rank KV cache compression with token-adaptive rank selection for LLM inference.
importance: 4
category: Research
---

This project compresses the KV cache by applying SVD to projection layers with token-adaptive rank selection, achieving 60% compression with minimal loss.

The PIM-enabled system schedules operations on HBM-based PIM units or xPU, achieving 1.58x and 1.96x speedups compared with state-of-the-art GPU-only and GPU-PIM designs. The work is under review at MICRO.
