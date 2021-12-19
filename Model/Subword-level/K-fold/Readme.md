## K-fold validation

The best models to our findings for Authorship Attribution in Bangla were the subword tokenized models pre-trained with news corpus. To test their robustness, K-fold cross-validation was performed on both BAAD6 and BAAD16 datasets.

### Reproducibility
To reproduce the K-fold tests:
- Clone the repository.
- Download --- checkpoint files from [this drive link]() and put them inside `Model Checkpoints` folder. Maintain the folder structure as in the drive folder.
- Make sure you have Python3.x
- Install requirements.txt. `pip install requirements.txt`
- Run the python notebooks (extra dependencies are installed in the notebook)


If we had used git-lfs, these would have been the commands. But we couldn't. So please ignore these. Retained for reference purposes.
- Install `git-lfs` from https://git-lfs.github.com/
- Make sure to `export GIT_LFS_SKIP_SMUDGE=1` before cloning to avoid downloading all checkpoints
- Do `git lfs pull --include="<filename>"` to include checkpoints as required. See [this](https://sabicalija.github.io/git-lfs-intro/) for more on how to use git-lfs
- If you are brave and want to download all checkpoints (~GB): `git lfs pull`