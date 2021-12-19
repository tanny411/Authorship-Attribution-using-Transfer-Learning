## K-fold validation

The best models to our findings for Authorship Attribution in Bangla were the subword tokenized models pre-trained with news corpus. To test their robustness, K-fold cross-validation was performed on both BAAD6 and BAAD16 datasets.

### Reproducibility
To reproduce the tests:
- Clone the repository.
- Make sure to `export GIT_LFS_SKIP_SMUDGE=1` before cloning to avoid downloading all checkpoints.
- Do `git lfs pull --include=<filename>` to include checkpoints as required. See [this](https://sabicalija.github.io/git-lfs-intro/) for more on how to use git-lfs.
- Run the python notebooks (dependencies are installed in the notebook)