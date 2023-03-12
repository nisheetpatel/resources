---
{"dg-publish":true,"permalink":"/my-coding-setup/","created":"","updated":""}
---


## My coding setup

-   Language: [Python](https://www.python.org/)
-   Package manager: [conda](https://docs.conda.io/en/latest/)/[mamba](https://github.com/mamba-org/mamba)
-   Version control: [Git](https://git-scm.com/)/[Github](https://github.com/)
-   IDE: [VSCode](https://code.visualstudio.com/)
-   Linter: [pylint](https://github.com/PyCQA/pylint)
-   Auto-formatter: [black](https://github.com/psf/black)
-   Documentation: [Obsidian](https://obsidian.md/)


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/v-scode-extensions/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">





#### VSCode extensions

-   [Docker](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) for containerized applications (to be deployed on clusters)
-   [Github Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) as an AI pair programmer
-   [Gitlens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) to supercharge git: see who did what and when in-line
-   [isort](https://marketplace.visualstudio.com/items?itemName=ms-python.isort) to automatically organize python imports
-   [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) for markdown files
-   [Micromamba](https://marketplace.visualstudio.com/items?itemName=corker.vscode-micromamba) for [conda](https://docs.conda.io/en/latest/)/[mamba](https://github.com/mamba-org/mamba) environment management
-   [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense) to autocomplete filenames
-   [Pylance](https://marketplace.visualstudio.com/items?itemName=ms-python.vscode-pylance) for python basics
-   [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) for python basics
-   [Tabnine AI Autocomplete](https://marketplace.visualstudio.com/items?itemName=TabNine.tabnine-vscode) as an AI pair programmer
-   [Vim](https://marketplace.visualstudio.com/items?itemName=vscodevim.vim) for emulating vim in VSCode

</div></div>



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/tips-for-collaborative-projects/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">





#### Tips for collaborative projects

> [!tip] Common settings
> Setup the same linter, IDE, and code auto-formatter. This way, there's no need to argue about silly things and the whole team can focus on what matters - the actual code. Refer to [[02 Programming#My coding setup\|my coding setup]] for details.

> [!info] Workflow
> Agree on a workflow if you can. I typically follow the [feature branch workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow). The article does a good job explaining the idea, but the tl;dr is to work on a separate branch for each new feature and not directly on master so you're not disturbing everyone else's work by pushing.

</div></div>
