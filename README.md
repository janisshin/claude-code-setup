# Claude Code Setup

1. Install [Docker](https://www.docker.com/products/docker-desktop/).
2. Install [VS Code](https://code.visualstudio.com/download).

3. Install DevContainer extension in VS Code.
4. Clone this repo in VS Code.
5. Reopen the repo within the DevContainer.
6. Run
```
chmod +x setup.sh
./setup.sh
```
7. Run
```
cp .env.example .env && chmod 600 .env
```
8. Generate your [Anthropic API key](https://console.anthropic.com/login?selectAccount=true&returnTo=%2Fsettings%2Fkeys%3F)
9. Run
```
source .env && claude
```




[List of Anthropic models](https://docs.anthropic.com/en/docs/about-claude/models/overview)





# Using Roo

Roo is a VSCode extension that communicates with Claude Code via Aider, using your Anthropic API key. You will be using Poetry to manage the environment, and `aider` will act as your Claude-powered AI coding assistant.

For Windows, 
You must have Python with a version >=3.10 and <3.13 installed (this can be through conda). 
You also need to have gitbash installed.  

On Windows, open the terminal (ctrl + J on VS Code) and go to command prompt. Install `pipx` by running 
```
python -m pip install --user pipx
```

A warning will pop up telling you where `pipx` was installed. 
Copy that path and then run this command to add pipx to your search path. 

```
path\from\warning\message\pipx.exe ensurepath
```
Close the terminal by clicking the garbage can. Shut down VS Code. 
Reopen VS Code. 
Open the terminal again (ctrl + J) and install poetry
```
pipx install poetry
```
`Poetry` is a environment manager like Conda or venv. 

You want to create a new environment from which to run Roo, so we'll create one with this command. I've named my environment `roo-env`, but you can choose whatever name you want. 
```
poetry init --name roo-env --python ">=3.11,<3.13"
```

It'll ask you a bunch of questions to set up the environment. You can just leave all the fields blank if you choose and edit the resulting `pyproject.toml` file later. Here are some of my example answers: 
```
This command will guide you through creating your pyproject.toml config.

Version [0.1.0]:
Description []:  For using Roo 
Author [Janis Shin <jshin1@uw.edu>, n to skip]:  
License []:  MIT

Would you like to define your main dependencies interactively? (yes/no) [yes] yes

Package to add or search for (leave blank to skip): numpy
Found 120 packages matching numpy
Showing the first 10 matches

Enter package # to add, or the complete package name if it is not listed []:
 [ 0] numpy
 [ 1]
 >0
1.26.4
```
...and so on and so forth. It'll ask you if you want to define development dependencies as well. This is stuff like 
- Interactive tools (`ipython`, `jupyter`)
- Testing frameworks (`pytest`, `unittest`, etc.)
- Linters and formatters (`black`, `flake8`, `pylint`)
- Type checkers (`mypy`)
- Debugging tools (`ipdb`, `debugpy`)

Usually, I just install `ipykernel` and `jupyterlab` here. If you've already added those to the main dependencies above, that's totally fine. 
```
poetry install --no-root
```
poetry env activate    

Create a 





