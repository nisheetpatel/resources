---
{"dg-publish":true,"permalink":"/02-programming/","created":"","updated":""}
---


#resources #programming #python #software

# Programming

If you find it useful, here's [[My coding setup\|my coding setup]] and here are some [[Tips for collaborative projects\|tips for collaborative projects]]. I am a mostly self-taught programmer, and as much as it pains me to admit, I started with Matlab. However, I can barely remember those days, and thanks to these resources, I consider myself a decent python developer.


<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/arjancodes/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">





## Arjancodes

##### Software design course + pythonic design patterns

By far, the best course out there that not only offers an introduction to the formal concepts but goes through the practical details is Arjan's [Software Design Mindset](https://www.arjancodes.com/mindset). For anyone who learns like I do, this is an absolute gem. 

There is also an extension that includes Pythonic design patterns that I cannot find the link for but can highly recommend once you get through the first course.

Together, they're so comprehensive and manage to cover every aspect of modern pythonic programming. It has dramatically increased my productivity as a developer and made the whole process so much more enjoyable.

##### YouTube

If you cannot afford the course, I would still recommend [Arjancodes' YouTube channel](https://www.youtube.com/c/arjancodes). He has some fantastic videos that put the principles into practice. Some of my early favorites, before I eventually decided to take his course, were [cohesion and coupling](https://www.youtube.com/watch?v=eiDyK_ofPPM), [composition vs inheritance](https://www.youtube.com/watch?v=0mcP8ZpUR38), [SOLID design principles](https://www.youtube.com/watch?v=pTB30aXS77U), [abstraction and composition](https://www.youtube.com/watch?v=ka70COItN40&t=3s), the other videos on refactoring data science projects (pt [2](https://www.youtube.com/watch?v=Tx4AxbQNv3U), [3](https://www.youtube.com/watch?v=8fFqakxhW84)), and then some others on using [dataclasses](https://www.youtube.com/watch?v=vRVVyl9uaZc), [pydantic](https://www.youtube.com/watch?v=Vj-iU-8_xLs), [ABC vs protocol](https://www.youtube.com/watch?v=xvb5hGLoK0A&t=248s). that make OOP life easier.


</div></div>



<div class="transclusion internal-embed is-loaded"><a class="markdown-embed-link" href="/my-coding-setup/" aria-label="Open link"><svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="svg-icon lucide-link"><path d="M10 13a5 5 0 0 0 7.54.54l3-3a5 5 0 0 0-7.07-7.07l-1.72 1.71"></path><path d="M14 11a5 5 0 0 0-7.54-.54l-3 3a5 5 0 0 0 7.07 7.07l1.71-1.71"></path></svg></a><div class="markdown-embed">





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


</div></div>


## Books

- [The good research code handbook](https://goodresearch.dev/index.html)
- [Learn Python the hard way by Zed Shaw](https://rupert.id.au/python/book/learn-python3-the-hard-way-nov-15-2018.pdf) 