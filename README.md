# Data Science Project

#### Installation
First, install a virtual environment library.
This may vary based for Windows, Mac, and Linux users.
Then,
```
# Create the virtual environment
python3.7 -m venv env

# Activate it
source env/bin/activate

# Install dependencies for the project
pip3 install requirements.txt
```

After adding a new library, run 
`pip3 freeze > requirements.txt` 
to keep track of it.

#### Notebooks
Rather than tracking notebooks in git, a better code review experience,
the project managers
have decided it is better to commit changes as python scripts
rather than Jupyter notebooks.

To track notebooks in git as python scripts, run the following prior to committing.
```
jupyter nbconvert --to script <filename>
```
This creates a .py version of the notebook that does not have a 
Json structure or saved outputs. This will allow us to see code changes easily.
A library (`p2j`) has been included in the dependencies to enable
conversion of the script back to a Jupyter notebook.