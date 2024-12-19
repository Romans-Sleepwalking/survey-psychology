# Survey

### Psychology


---

### Technical prerequisites

#### Install pyenv
Run the following in the Terminal:
```shell
git clone https://github.com/pyenv/pyenv.git ~/.pyenv
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bash_profile
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bash_profile 
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n eval "$(pyenv init -)"\nfi' >> ~/.bash_profile
```
Then, restart the Terminal.

#### Update pyenv and install Python 3.12.7 using it
Run the following in the Terminal:
```shell
cd $(pyenv root)
git checkout master
git pull
pyenv install 3.12.7
```

#### Set up poetry
1. Open the Terminal
2. Confirm that the `poetry` has been installed correctly. Please run `poetry --version` (we require poetry version `>= 1.6.0`).
3. Change the current working directory to the `survey-psychology` project directory: e.g., `cd ~/survey-psychology`.
4. Make sure you are using a suitable Python version. Please run `poetry env use 3.12.7` (for python 3.12.7, as an example)
5. Install necessary dependencies. Please run `poetry shell` and `poetry install`.
  * You can see the name of the created environment by calling `poetry env list`.
  * More on managing poetry environments is [available here](https://python-poetry.org/docs/managing-environments/).

#### Set up poetry in Jupyter
1. Create an IPython kernel: `poetry run ipython kernel install --user --name=python3-12-survey-psychology`
2. In the notebook, change from the default kernel, to the one you have just made: 'Kernel' > 'Change Kernel'.
