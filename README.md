# ML Foundations

[![tests](https://github.com/helenalm04/ml-foundations/actions/workflows/tests.yml/badge.svg)](https://github.com/helenalm04/ml-foundations/actions/workflows/tests.yml)

Lecture-style notes on the foundations of machine learning, each with a from-scratch implementation checked against a reference library.

## How each notebook is organised

Each topic is one notebook, with the same sections in the same order:

1. **Explanation**: a summary, the intuition, then the mathematical formulation.
2. **Implementation**: a from-scratch version in NumPy or PyTorch.
3. **Experiments**: short plots and results.
4. **Checks against a reference**: asserts comparing the implementation with scikit-learn or PyTorch.
5. **Questions to test yourself**: questions and follow-ups, then gotchas and references.

ML system design is a Markdown file with no code, so it skips sections 2 to 4.

## Topics

| # | Topic | nbviewer | Area | Status |
|---|---|---|---|---|
| 01 | [Bias-variance and regularisation](notebooks/01-bias-variance-regularisation.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/01-bias-variance-regularisation.ipynb) | Classical ML and stats | ⬜ |
| 02 | [Linear and logistic regression](notebooks/02-linear-logistic-regression.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/02-linear-logistic-regression.ipynb) | Classical ML and stats | ⬜ |
| 03 | [Model evaluation](notebooks/03-model-evaluation.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/03-model-evaluation.ipynb) | Classical ML and stats | ⬜ |
| 04 | [Trees and boosting](notebooks/04-trees-and-boosting.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/04-trees-and-boosting.ipynb) | Classical ML and stats | ⬜ |
| 05 | [PCA and SVD](notebooks/05-pca-svd.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/05-pca-svd.ipynb) | Classical ML and stats | ⬜ |
| 06 | [Backpropagation](notebooks/06-backpropagation.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/06-backpropagation.ipynb) | Deep learning | ⬜ |
| 07 | [Optimisers](notebooks/07-optimisers.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/07-optimisers.ipynb) | Deep learning | ⬜ |
| 08 | [Initialisation, normalisation and dropout](notebooks/08-init-normalisation-dropout.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/08-init-normalisation-dropout.ipynb) | Deep learning | ⬜ |
| 09 | [CNNs](notebooks/09-cnns.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/09-cnns.ipynb) | Deep learning | ⬜ |
| 10 | [Attention and transformers](notebooks/10-attention-transformers.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/10-attention-transformers.ipynb) | Deep learning | ⬜ |
| 11 | [EM and Gaussian mixtures](notebooks/11-em-gaussian-mixtures.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/11-em-gaussian-mixtures.ipynb) | Generative and probabilistic | ⬜ |
| 12 | [VAEs](notebooks/12-vaes.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/12-vaes.ipynb) | Generative and probabilistic | ⬜ |
| 13 | [Diffusion](notebooks/13-diffusion.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/13-diffusion.ipynb) | Generative and probabilistic | ⬜ |
| 14 | [LLMs](notebooks/14-llms.ipynb) | [view](https://nbviewer.org/github/helenalm04/ml-foundations/blob/main/notebooks/14-llms.ipynb) | LLMs and system design | ⬜ |
| 15 | [ML system design](notebooks/15-ml-system-design.md) | — | LLMs and system design | ⬜ |

The nbviewer links are a fallback for when GitHub's notebook viewer fails to render.

To add a topic, copy `TEMPLATE.ipynb` into `notebooks/` and add a row to the table.

## Running the notebooks

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

Run all checks. This executes every notebook top to bottom, the same way CI does:

```bash
pytest --nbmake notebooks/
```

## License

MIT. See [LICENSE](LICENSE).
