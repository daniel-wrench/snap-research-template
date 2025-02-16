# Repository Template for Reproducible Research

This simple project structure template repository is adapted from [https://github.com/UtrechtUniversity/simple-python-template]. **Click "Use this template"** at the top of this page to create a new repository with the same folder structure, and then add your own files and edit this README for your particular project.

If you plan to develop a package, check the [template repository for a Python package](https://github.com/UtrechtUniversity/re-python-package).

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
*Recommended: change based on your specific files*

The project structure distinguishes three kinds of folders:
- read-only (RO): not edited by either code or researcher
- human-writeable (HW): edited by the researcher only.
- project-generated (PG): folders generated when running the code; these folders can be deleted or emptied and will be completely reconstituted as the project is run.


```
.
├── .gitignore
├── LICENSE
├── README.md
├── requirements.txt   <- Package requirements needed to execute the code in `scripts/`
├── data               <- All project data, ignored by git
│   ├── processed      <- The final, canonical data sets for modeling. (PG)
│   ├── raw            <- The original, immutable data dump. (RO)
│   └── temp           <- Intermediate data that has been transformed. (PG)
├── docs               <- Documentation notebook for users (HW)
│   ├── manuscript     <- Manuscript source, e.g., LaTeX, Markdown, etc. (HW)
│   └── reports        <- Other project reports and notebooks (e.g. Jupyter, .Rmd) (HW)
├── results
│   ├── figures        <- Figures for the manuscript or reports (PG)
│   └── output         <- Other output for the manuscript or reports (PG)
└── src                <- Source code for this project (HW)

```

## Add a citation file
Create a citation file for your repository using [cffinit](https://citation-file-format.github.io/cff-initializer-javascript/#/)

## License

This project is licensed under the terms of the [MIT License](/LICENSE).
