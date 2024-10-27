# Template
 This is strictly following [this awesome guide](https://maeda.pm/2024/03/03/python-poetry-and-vs-code-2024/). I just added a couple of preliminary steps and some windows/powershell versions of the commands.

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
```
J. Type Poetry Install (fingers crossed, no errors).
I had to change my python interpretor version in `VScode` to reflect the latest version that I had installed.
To ensure that Visual Studio Code uses the same Python version as your latest version in PowerShell, follow these steps:

1. **Check Python Version in PowerShell:**
   Open PowerShell and run:
   ```powershell
   python --version
   ```

2. **Find Python Path:**
   In PowerShell, find the path to the Python executable:
   ```powershell
   Get-Command python
   ```

3. **Update Python Interpreter in Visual Studio Code:**
   - Open Visual Studio Code.
   - Press `Ctrl+Shift+P` to open the Command Palette.
   - Type `Python: Select Interpreter` and select it.
   - Choose the Python interpreter that matches the path found in PowerShell.

4. **Verify Python Version in Visual Studio Code:**
   - Open a terminal in Visual Studio Code.
   - Run:
     ```sh
     python --version
     ```

This should ensure that Visual Studio Code uses the same Python version as your latest version in PowerShell.

K. Type poetry shell and you should be in the environment you created.
L. Type:
```sh
poetry add numpy
```
M. Adding it into VS Code:
```sh
poetry env info
```

N. Add the path to the clipboard:
Windows:
```sh
poetry env info --path | Set-Clipboard
```
Mac:
```sh
poetry env info --path |pbcopy
```

Open command palette (CNTRL + SHIFT + P) and select add manually

O. OMG, just choose the right interpreter and things should be fine!
