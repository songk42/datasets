# Atomic Datasets

This repository contains the following 3D molecular datasets:
- QM9
- GEOM (Drugs)
- tmQM

as well as the following toy datasets:
- Platonic Solids
- 3D Tetris Pieces

## Installation
Install directly from GitHub with [pip](https://pypi.org/project/pip/):
```bash
pip install git+https://github.com/atomicarchitects/datasets
```
or [uv](https://docs.astral.sh/uv/getting-started/installation/):
```bash
uv pip install git+https://github.com/atomicarchitects/datasets
```

## Example
```python
from atomic_datasets.datasets import QM9Dataset

dataset = QM9Dataset(
    root_dir="data/qm9",
    check_with_rdkit=True,
)

for graph in dataset:
	# graph is a dictionary.
	print(graph["nodes"], graph["properties"])
```

## Citation

If you use this repository, please cite the original papers for the relevant datasets:
- QM9:
```
@article{qm9,
	author = {Ramakrishnan, Raghunathan and Dral, Pavlo O. and Rupp, Matthias and von Lilienfeld, O. Anatole},
	journal = {Scientific Data},
	number = {1},
	pages = {140022},
	title = {Quantum chemistry structures and properties of 134 kilo molecules},
	volume = {1},
	year = {2014}
}
```
- GEOM:
```
@article{geom,
	author = {Axelrod, Simon and G{\'o}mez-Bombarelli, Rafael},
	journal = {Scientific Data},
	number = {1},
	pages = {185},
	title = {GEOM, energy-annotated molecular conformations for property prediction and molecular generation},
	volume = {9},
	year = {2022}
}
```
- tmQM:
```
@article{tmQM,
	author = {Balcells, David and Skjelstad, Bastian Bjerkem},
	journal = {Journal of Chemical Information and Modeling},
	month = {12},
	number = {12},
	pages = {6135--6146},
	title = {tmQM Dataset---Quantum Geometries and Properties of 86k Transition Metal Complexes},
	volume = {60},
	year = {2020}
}
```
- 3D Tetris:
```
@phdthesis{
    author={Smidt, Tess E.},
    year={2018},
    title={Toward the Systematic Design of Complex Materials from Structural Motifs},
    journal={ProQuest Dissertations and Theses},
    pages={200},
    note={Copyright - Database copyright ProQuest LLC; ProQuest does not claim copyright in the individual underlying works; Last updated - 2023-03-04},
    language={English},
    url={https://www.proquest.com/dissertations-theses/toward-systematic-design-complex-materials/docview/2137540057/se-2},
}
```


