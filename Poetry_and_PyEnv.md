## Working with Pyenv and Poetry | THER RIGHT WAY!!! UBUNTU 22.04

1. Install pyenv
```bash
sudo apt install -y make build-essential libssl-dev zlib1g-dev \
libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl
```
2. Install pyenv
```bash
curl https://pyenv.run | bash
```

3. Install poetry
```bash
curl -sSL https://install.python-poetry.org | python3 -
```
* Configure poetry to create virtual environments **inside the project's root directory**
```bash
poetry config virtualenvs.in-project true
```
4. Install the python especific version you want in your system
```bash
pyenv install 3.8
```
* Verify installation
```bash
pyenv versions
```
5. Inside your project root directory set the local python version using pyenv
```bash
pyenv local 3.8.16
```
* this is going to create a file called **.python-version** and _poetry_ will used it to based the python interpreter
6. Create poetry virtual enviroment
```bash
poetry env use 3.8.16
```
* Now you should have .venv inside your project, open it and see if inside _bin_ folder the puthon executable have the same version you want like _python3.8_
