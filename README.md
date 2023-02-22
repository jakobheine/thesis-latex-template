# WIP! Master Thesis LaTeX

For the creation of this thesis LaTeX template, the [LaTeX Master template](https://github.com/a-czyrny/LaTeX-Master-Vorlage) from [Alexander Czyrny](https://github.com/a-czyrny) was used, which is licensed under [Attribution-NonCommercial-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-nc-sa/4.0?ref=chooser-v1). Furthermore, the template was translated and adjusted to own needs.

# Getting started

## MacOS with Apple Silicon

1. Install *MacTex*, preferably without GUI, as we are going to use *Visual Studio Code (VSC)*: ```brew install --cask mactex-no-gui``` (don't be confused by the multiple password requests)
2. Restart your terminal
3. Update the LaTeX packages by running: ```sudo tlmgr update --self && sudo tlmgr update --all``` 
4. In VSC: Install the [LaTeX Workshop extension](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop), after the installation, restart VSC

## Everything else

Until now, the setup was only tested on MacOS with Apple Silicon chips. If you use a different system, try the guide provided [here](https://medium.com/@rcpassos/writing-latex-documents-in-visual-studio-code-with-latex-workshop-d9af6a6b2815) for the steps 1.-3. above and feel free to create a PR to update the README with the needed steps for your system.

9_misc/figures/signature.png -> add own signature