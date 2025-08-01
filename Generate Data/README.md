The following folder contains scripts to generate the synthetic data. Run the ipynb file `Generate Data.ipynb` to create the data. The project uses the UV venv manager. If you have UV installed, run `uv sync` and `uv venv` to replicate the env. Otherwise use pyproject.toml to get the correct dependencies.

Going though  `Generate Data.ipynb`  will generate data and and put it in the postgres initdb folder. The data will be used to populate the database when it is created.
