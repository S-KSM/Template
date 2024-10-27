# Template
 This is a dev template! 
 
 Step 1. Install Python, make sure to add it to the path
 Step 2. Install PipX:
 ```sh
python -m pip install --user pipx
python -m pipx ensurepath
```
Step 3: Instal poetry:
```sh
pipx install poetry
```

A. Create a github managed repository
B. Open VS code
C. Open terminal
D. Go to code root:
```sh
poetry init
```
E. follow the wizard and create the project.
F. Make a new project subdirectory and call it myapp.
G. Make sure the pyproject.toml reads:
```YAML

[tool.poetry]
name="myapp"
```
H.create a main.py into the myapp subdirectory

(in windows with powershell):

```sh
New-Item -ItemType File -Path .\myapp\main.py
```
I. Create a simple program like:
```python

if __name__=="__main__":
    print("Happy Birthday")

J. Type Poetry Install (fingers crossed)