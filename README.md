# Repository Template for Reproducible Research

This simple project structure template repository is adapted from [https://github.com/UtrechtUniversity/simple-python-template]. **Click "Use this template"** at the top of this page to create a new repository with the same folder structure, and then add your own files and edit this README for your particular project.

If you plan to develop a package, check the [template repository for a Python package](https://github.com/UtrechtUniversity/re-python-package).

See [here](https://github.com/DenisMot/Python-minimal-install) for a useful guide to installing a minimal Python environment and setting up in VS Code and conda.

## How to run this code 

#### Clone this repository

```sh
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
```

#### Change directory to this folder

```sh
cd YOUR-REPO-NAME
```

#### Set up virtual environment
- Create a virtual environment: `python -m venv env`
- Activate the environment:
    - Windows: `.\env\Scripts\activate`
    - Unix/macOS: `source env/bin/activate`
- Install required packages: `pip install -r requirements.txt`
    - If you haven't yet set up this file, you can first install the required packages, then use `pip freeze > requirements.txt` to write all the dependencies (and their versions) to this file. *Note that this can be a bit overkill with the number of dependencies listed: see [here](https://calmcode.io/course/pip-tools/compile) for an improved method.*

#### Execute code
*For example: change these based on your specific files, and add detail about what each step involves*
```
python scripts/01_get_data.py
python scripts/02_clean_data.py
python scripts/03_analysis.py
```

## Project Structure
*Recommended: change based on your specific files. For example, you may also want a `models/` or `notebooks/` folder.*

```
.
├── README.md          <- Overview of the project, how to install and use 
├── LICENSE            <- License for open-source projects
│── CITATION.cff       <- Citation file for academic use
├── .gitignore         <- Files to ignore (e.g., __pycache__, logs, data)
├── requirements.txt   <- Dependencies (if using pip)
├── data               <- Data directory (typically ignored in version control)
│   ├── raw/           <- Raw input data (DO NOT MODIFY!)
│   └── processed/     <- Processed datasets
├── outputs            <- Outputs like figures, tables, reports
│   └── figs           <- Plots and figures
├── src                <- Source code for the project
│   ├── utils.py       <- Functions used by multiple scripts
└── scripts            <- Python/R/etc. scripts for for processing and analysing data
    ├── 01_get_data.py
    ├── 02_clean_data.py
    └── 03_analysis.py

```

## Add a citation file
Create a citation file for your repository using [cffinit](https://citation-file-format.github.io/cff-initializer-javascript/#/)

## License

This project is licensed under the terms of the [MIT License](/LICENSE).
