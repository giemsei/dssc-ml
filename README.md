# DSSC MACHINE LEARNING PROJECT

Author: G. Alessio, A. Campagnolo, M. Polo, G. Sarnelli

## Usage

### Create environment
```
conda env create -f environment.yml #create conda env
conda activate dssc-ml #activate conda env
pip install tweepy #see note below
#TBD
```

Note: `tweepy` isn't available on default channel and currently `conda env export`, `conda env create -f`, ecc. don't work with conda-forge. So it must be installed separately with `conda install -c conda-forge tweepy` or `pip install tweepy`. The former leads to a broken `environment.yml` when exporting, so the latter is preferable even if `conda env export` currently ignores `pip`-installed packages for no reason.

### Workflow

When you upload any modification in the (...), comment the commit with the modifications you've done. 

**To upload the files**
```
git add <filename>
git commit
git push
```

To update the environment file to match the environment:
```
conda env export --from-history > environment.yml
```
To update the environment to match the environment file:
```
conda env update --file environment.yml
```

Files structure:
1. `twitter-sport-politics.ipynb`
   1. *machine learning project exercise used as references*
2. `.notes/`
   1. *Personal notes backup*
3. `filename`
   1. *comment*
4. `filename`
   1. *comment*

...

Notes:
- `dateofthenote`: [notes] - `author`
- `dateofthenote`: [notes] - `author`
- `dateofthenote`: [notes] - `author`
...
