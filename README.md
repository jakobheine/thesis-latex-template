# 🚀 Master Thesis LaTeX Template

* Easy to use LaTeX template
* Styleguide approved for [HTW Berlin](https://www.htw-berlin.de/)
* Step by step guide to get your thesis formatting to final level

🚀 "I have no idea about LaTeX, but I want to use it anyway." 🚀

# ⚙️ Setup your system (30 minutes)

## 🍏 MacOS with Apple Silicon

1. Install *MacTex*, preferably without GUI, as we are going to use *Visual Studio Code (VSC)*: ```brew install --cask mactex-no-gui``` (don't be confused by the multiple password requests)
2. Restart your terminal
3. Update the LaTeX packages by running: ```sudo tlmgr update --self && sudo tlmgr update --all``` 
4. In VSC: Install the [LaTeX Workshop extension](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop), after the installation, restart VSC

## Everything **not** MacOS with Apple Silicon

Until now, the setup was only tested on MacOS with Apple Silicon chips. If you use a different system, try the guide provided [here](https://medium.com/@rcpassos/writing-latex-documents-in-visual-studio-code-with-latex-workshop-d9af6a6b2815) for the steps 1.-3. above and feel free to create a PR to update the README with the needed steps for your system.

9_misc/figures/signature.png -> add own signature
- remove main.ist file, add to .gitignore

# 🏃🏼‍♂️ Getting started (10 minutes)

1. On the [Github-page](https://github.com/jakobheine/thesis-latex-template) of this repository, click the **green "Use this template"** button and create a copy of this repository. **Don't clone this repository, as you don't have permissions to overwrite any files**.
2. I advice you to [generate & publish a SSH key on GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent), so that you can commit often, because one main advantage from LaTeX compared to Word is that you can leverage the versioning of the files using Git.
3. Make sure you setup your system.
4. Make sure to check out the "Add some spice to your setup section" to skyrocket productity.
5. Continue with exploring the structure of the template and get going.

# 🌶  Add some spice️ to your setup

One main advantage of using VSC is that you can install an extension for almost everything, here some lifehacks:

## Use [Grammarly](https://www.grammarly.com/) 

Grammarly is an AI-powered grammar & language checker. You write your sentences once in VSC -> it automatically formats it using LaTeX & it automatically shows you how bad your English is (😄) and gives you very good recommendations on how to formulate it better or even automatically does it for you. Additionally, you can configure how you want to sound, who your audience is and in which language you are writing (American/British/Canadian english). Sold?

1. Install [this VSC extension](https://marketplace.visualstudio.com/items?itemName=znck.grammarly) and configure it based on your needs.
2. Create an account on [Grammarly](https://www.grammarly.com/) and connect it with the VSC extension.
3. (optional)  💰 Get a subscription. Some features are only available by getting a subscription, but if you ask me, it is worth every penny.

# 🙌🏼 Credits

For the creation of this thesis LaTeX template, the [LaTeX Master template](https://github.com/a-czyrny/LaTeX-Master-Vorlage) from [Alexander Czyrny](https://github.com/a-czyrny) was used, which is licensed under [Attribution-NonCommercial-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-nc-sa/4.0?ref=chooser-v1). Furthermore, the template was translated and adjusted to own needs.

# 👩🏼‍⚖️ License

**Apache License 2.0**, aka "Just use it for whatever reason, I am happy to help. 🌝" 