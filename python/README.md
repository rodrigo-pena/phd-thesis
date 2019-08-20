# `python/`

## About

Python code for re-running the experiments and reproducing the figures in the thesis.



## Reproducibility

The code in this folder depends on the [Graph Signal Sampling and Recovery (GSSR)][gssr] repository. Open a terminal window, navigate to a folder where you want to keep the GSSR repository, and type

```
git clone https://github.com/rodrigo-pena/gssr.git
```

to clone a local copy to your system. Then, to guarantee proper functioning of the code in `phd-thesis/python/`, you will need to set the HEAD of the GSSR repository to a specific commit, by typing

```
git checkout c8721f6e6b6ee20d58903bdcdbff068fc06d72e1
```

Finally, check the GSSR [README][gssr-readme] for instructions on how to install the needed dependencies and set up a working environment.



Now you will need to tell the Python files in `phd-thesis/python/` where the GSSR repository is in your system. If you are working on MacOS and you have cloned the  `gssr/` folder to the same base directory as `phd-thesis/`, then you probably do not have to do anything and can already run the files that you want. Otherwise, every `.py` and `.ipynb` file (with the exception of `helper.py`) has a header code that reads

```python
cmd_folder = '../../gssr' # Insert here the string pointing to the gssr root folder

# Make sure the gssr folder is in the python path
import os, sys
if cmd_folder not in sys.path:
    sys.path.insert(0, cmd_folder)
```

You will need to replace the string `'../../gssr'` with the path to the `gssr/` folder that you cloned to your computer.



*Remarks*:

- At the time of writing, the GSSR repository was not yet ready to be fully packaged into a Python module, which would have made things easier, requiring simply a call to `pip install` . The solution presented is "hacky", but at least it guarantees that the code in `phd-thesis/python/` will run without errors.
- Remember  to make sure that you run the programs in this repository under the gssr environment. See the "Using the repository" section in the GSSR [README][gssr-readme] if in doubt.



## Content

- `helper.py`
  
  - A collection of miscellaneous helper functions.
  
- `pt_bsds.py`
  
  - Code for the phase transition experiments with the [BSDS300][bsds300] dataset.
  
- `pt_email_eu_core.py`
  
  - Code for the phase transition experiments with the [email-EU-core][email-eu-core] dataset.
  
- `pt_sbm.py`

  - Code for the phase transition experiments with unbalanced Stochastic Block Model (SBM) graphs.

- `pt_ssbm.py`

  - Code for the phase transition experiments with symmetric SBM graphs.

- `pt_swiss_national_council.py`

  - Code for the phase transition experiments with the Swiss National Council data.

- `run_all_experiments.sh`

  - Bash script for running all the experiments in the thesis.

- `run_experiment_1.sh`

  - Bash script for running the phase transition experiments involving uniform sampling and graph total-variation (G-TV) interpolation.

- `run_experiment_2.sh`

  - Bash script for running the phase transition experiments involving uniform sampling and Dirichlet form interpolation.

- `run_experiment_3.sh`

  - Bash script for running the phase transition experiments involving naive coherence sampling and G-TV interpolation.

- `run_experiment_4.sh`

  - Bash script for running the phase transition experiments involving jump-set coherence sampling and G-TV interpolation.

- `ch1_introduction.ipynb`

  - Jupyter notebook for reproducing the figures of Chapter 1, "Introduction".

- `ch6_numerical_tour.ipynb`

  - Jupyter notebook for reproducing the figures of Chapter 6, "A numerical tour".

- `thesis.mplstyle`

  - Matplotlib style file for customizing the display properties of the figures generated in `ch1_introduction.ipynb` and `ch6_numerical_tour.ipynb`.

- `epfl_colors_hex.txt` and `epfl_colors_hex.pkl`

  - EPFL's [official color palette][brand-identity].

  



[brand-identity]: https://inside.epfl.ch/corp-id/en/brand-identity/
[email-eu-core]: http://snap.stanford.edu/data/email-Eu-core.html
[bsds300]:  https://www2.eecs.berkeley.edu/Research/Projects/CS/vision/bsds/
[gssr]: https://github.com/rodrigo-pena/gssr
[gssr-readme]: https://github.com/rodrigo-pena/gssr/blob/c8721f6e6b6ee20d58903bdcdbff068fc06d72e1/README.md