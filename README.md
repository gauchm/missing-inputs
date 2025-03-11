# How to deal with missing input data

Accompanying code for the paper [**"How to deal w___ missing input data"**](https://doi.org/10.31223/X50M8N)

    Gauch, M., Kratzert, F., Klotz, D., Nearing, G., Cohen, D. and Gilon, O.:
    How to deal w___ missing input data, EarthArXiv preprint, 2025. 

The code in this repository, together with the [`neuralhydrology`](https://github.com/neuralhydrology/neuralhydrology) Python package, was used to produce all results and figures in our paper.
If you want to play around and train models yourself, we recommend taking a look at the [neuralhydrology documentation](https://neuralhydrology.readthedocs.io/), which also contains some tutorials on how to get started.

## Contents of this repository
- `missing-inputs.ipynb` -- Jupyter notebook to reproduce figures from the paper.
- `results/` -- Folder with model weights, configs, and predictions used in `missing-inputs.ipynb` (available on [Zenodo](https://doi.org/10.5281/zenodo.15008460), see below).
- `patches/` -- Contains patches for local modifications to reproduce experiments from the paper.

## Required setup
1. Clone neuralhydrology: `git clone https://github.com/neuralhydrology/neuralhydrology.git`
2. Install an editable version of neuralhydrology: `cd neuralhydrology && pip install -e .`.
3. Download the following data:
   1. the CAMELS US dataset (CAMELS time series meteorology, observed flow, meta data, version 1.2) from [NCAR](https://ral.ucar.edu/solutions/products/camels) into some data directory (has to match `data_dir` in the config files).
   2. the extended Maurer and NLDAS forcings set available on HydroShare: [Maurer](https://doi.org/10.4211/hs.17c896843cf940339c3c3496d0c1c077), [NLDAS](https://doi.org/10.4211/hs.0a68bfd7ddf642a8be9041d60f40868c).
   3. the models, results, and config files from this paper avaliable on [Zenodo](https://doi.org/10.5281/zenodo.15008460).
4. Note that to reproduce the experiments, local modifications to NeuralHydrology are necessary. To do so, apply the patches in the `patches/` directory: `git apply patches/experiment-N.patch`.

## Citation
```bib
@article{gauch2025missing,
    title = {How to deal w\_\_\_ missing input data},
    author = {Gauch, M. and Kratzert, F. and Klotz, D. and Nearing, G. and Cohen, D. and Gilon, O.},
    journal = {EarthArXiv},
    year = {2025},
    url = {https://eartharxiv.org/repository/view/8759/},
    doi = {10.31223/X50M8N}
}
```


