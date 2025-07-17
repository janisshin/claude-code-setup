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
