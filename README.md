# LLM Arithmetic - Manim Explainer

Manim animation source code for the video [How do LLMs add numbers?](https://www.youtube.com/watch?v=8VTzn8i34qo).

This repo is a code-backed explainer for one of the deceptively simple questions in language-model behavior: when a model answers an arithmetic prompt, what kinds of representations and transformations might be involved?

## What This Teaches

- How text tokens become vectors.
- How self-attention compares tokens through dot products and softmax weights.
- How value vectors, contextual embeddings, and nonlinear layers can change the information available at each position.
- Why arithmetic in LLMs is not the same as a symbolic calculator, even when the final answer looks simple.

## Repo Map

- `opening.py` - opening arithmetic examples.
- `tok_em.py`, `updated_embed.py` - token and contextual embedding scenes.
- `self_attention.py`, `compute_attn.py`, `value_vector.py` - attention mechanism scenes.
- `dot_product.py`, `softmax.py`, `softmax_dk.py` - vector similarity and normalization scenes.
- `relu.py`, `relu_l1.py`, `l1.py`, `mlpvsclt.py` - nonlinear activation and layer-comparison scenes.
- `addition_examples.py`, `text_cal.py`, `equal_sign_context.py` - arithmetic and prompt-context scenes.

## Running A Scene

Install Manim in a Python environment:

```bash
python -m venv .venv
source .venv/bin/activate
pip install manim
```

Render a preview scene:

```bash
manim -pql opening.py LLMScene
```

Render a more detailed attention scene:

```bash
manim -pql self_attention.py SelfAttentionAnimation
```

Use `-pqh` instead of `-pql` for a higher-quality render.

## Why This Exists

The video and code are meant to make model internals easier to reason about visually. The repo keeps the animation source public so the explanation is reproducible, inspectable, and reusable for future AI education work.

## Related Explainers

- [Hybrid Search + BM25](https://github.com/leannchen86/hybrid-search-bm25-manim)
- [CLIP Encoding](https://github.com/leannchen86/clip-encoding-manim)
- [Neural Superposition](https://github.com/leannchen86/neural-superposition-manim)
