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


# 🏃🏼‍♂️ Getting started (10 minutes)

1. On the [Github-page](https://github.com/jakobheine/thesis-latex-template) of this repository, click the **green "Use this template"** button and create a copy of this repository. **Don't clone this repository, as you don't have permissions to overwrite any files**.
2. I advice you to [generate & publish a SSH key on GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent), so that you can commit often, because one main advantage from LaTeX compared to Word is that you can leverage the versioning of the files using Git.
3. Make sure you [setup your system](https://github.com/jakobheine/thesis-latex-template#%EF%B8%8F-setup-your-system-30-minutes).
4. Make sure to [add some spice to your setup](https://github.com/jakobheine/thesis-latex-template#--add-some-spice%EF%B8%8F-to-your-setup) to skyrocket productity.
5. Continue with exploring the structure of the template and **start writing**.

# 🛠️ Structure & Wordmode of the template

* The heart of the application is the **main.tex** file in the root directory. Everything else you find in this repository is basically just imported somewhere in the main.tex file, or it is imported in a file that is imported to the main file, and so on...
* **CMD+S → main.tex → LaTeX → main.pdf** 

Every time you change a file and press safe, LaTeX takes the main.tex file, interprets it (aka importing all the imports) and creates the **main.pdf** you handover to your professor to get your well-deserved 1.0
* The only thing you most-likely need to change in the **main.tex** file are the lines from 27-30 to add your chapter structure:

```
\import{chapter/1_introduction/}{introduction.tex} \clearpage
\import{chapter/2_literature_review/}{literature_review.tex} \clearpage
\import{chapter/3_main_section/}{main_section.tex} \clearpage
\import{chapter/4_conclusion/}{conclusion.tex} \clearpage
```

* All style configurations like i.e. qoutation style, font size, ... are stored in the **resources/** directory. They are getting imported in the beginning of the **main.tex** and already follow best practices. You should not need to do any changes there. **❗️Changes at your own risk 😄**

* All references are stored in the file under **references/references.bib** You should store all your sources like journals, papers and books in this document to refer to it in your thesis. One entry stores all the meta-data information and could look like this.

```
@article{webster_guest_2002,
	title = {Guest {Editorial}:  {Analyzing} the {Past} to {Prepare} for the {Future}:  {Writing} a literature {Review}},
	language = {en},
	author = {Webster, Jane and Watson, Richard T},
	year = {2002},
	pages = {11},
	file = {Webster und Watson - Guest Editorial  Analyzing the Past to Prepare fo.pdf:/home/jakob/Zotero/storage/NHV75XKG/Webster und Watson - Guest Editorial  Analyzing the Past to Prepare fo.pdf:application/pdf},
}
```
To learn how to qoute this reference in your text check out the cheat sheet. Check out the Citavi setup guide to auto-refresh this bib-file whenever you find a new source.

* One thesis can have multiple chapters. One chapter can have multiple sections. One section can have multiple subsections. That's why all your text will end up in the **chapters/** directory.
This directory is structured as follows:
```
chapter/
├─ 1_chapter1/
│  ├─ section/
│  │  ├─ 1_section1_chapter1.tex
│  │  ├─ 2_section2_chapter1.tex
│  ├─ 1_chapter1.tex
├─ 2_chapter2/
│  ├─ images/
│  │  ├─ image1.png
│  │  ├─ image2.png
│  ├─ 2_chapter2.tex
├─ 99_miscellaneous/
│  ├─ abstract.tex
│  ├─ DoA.tex
```

* **DISCLAIMER:** How you structure the main text of your thesis is completely up to you. The following instructions are just an idea on how to structure it efficiently. 
    * The leadning numbers are just used to order the files in your editor, they are not mandatory. You can name the files however you want.
    * Every chapter folder has one top-level tex-file. You can write the whole chapter in this file, like shown in the example above for chapter2, or the 2_literature_review chapter in the template. 
    * If you want to **structure the chapter by using sections**, you can create a folder called i.e. "*section/*" where you create a tex-file for each section. In the top-level chapter-tex-file you specify the order of the sections., like shown in the example above for chapter1 or the 1_introduction chapter in the template.
    * If you want to use images in your thesis, you can create an **images/** directory on chapter or section level.
    * You can repeat this logic over-and-over for **subsections and subsubsections**. It is up to you to define how granular you want your thesis split.
    * On the very bottom you can have one directory called **99_miscellaneous/** for everything else around your thesis like the Abstract or the Declaration of Authenticity.
    * ❗️ If you create new chapters, make sure to refer to them in the **main.tex** file. ❗️

# 🌶  Add some spice️ to your setup

One main advantage of using VSC is that you can install an extension for almost everything, here some lifehacks:

## Use [Grammarly](https://www.grammarly.com/) 

Grammarly is an AI-powered grammar & language checker. You write your sentences once in VSC → it automatically formats it using LaTeX & it automatically shows you how bad your English is (😄) and gives you very good recommendations on how to formulate it better or even automatically does it for you. Additionally, you can configure how you want to sound, who your audience is and in which language you are writing (American/British/Canadian english). Sold?

1. Install [this VSC extension](https://marketplace.visualstudio.com/items?itemName=znck.grammarly) and configure it based on your needs.
2. Create an account on [Grammarly](https://www.grammarly.com/) and connect it with the VSC extension.
3. (optional)  💰 Get a subscription. Some features are only available by getting a subscription, but if you ask me, it is worth every penny.

## Use [Citavi](https://www.citavi.com/en) (or any other Reference Manager)

A reference manager like **Citavi** helps you in managing your references. (duh) The ideal workflow could look like this:
1. During your research on the web you find a promising paper/journal/website you want to refer in your thesis.
2. You press one button in your browser to add it to your references.
3. In the background, this press of the button auto-updates the **references.bib** file in your LaTeX document.
4. You can use the reference in your document.

To achieve this, you can use any reference manager that is capable of doing the second and third step. I prefer **Citavi**. Sold?

1. Create an account on [Citavi](https://www.citavi.com/en) to store your references online and i.e. also add references when you are reading them on your phone.
2. Downlaod Citavi on your machine. Setup a new document/project/thesis and configure it to auto-update the references.bib file in your LaTeX template.
3. Install the [Citavi browser plug-in "Picker"](https://www1.citavi.com/sub/manual5/en/installing_the_pickers.html).
4. (optional) Install Citavi on your phone if you want to read papers during travel.

# Cheat Sheet

The aim of this section is to provide you with an overview of how you can do certain things in the template. (e.g. which commands you have to use)

I wish I had this overview.. 😆

## 🔠 Font Style

|Command|Usecase|Example Usage|Example Output|Details|
|---|---|---|---|---|
|`\emph{Text}`|*Write italic*|`\emph{Mermaid Man}`|*Mermaid Man*| - |
|`\underline{Text}`|<ins>Underline text</ins>|`\underline{Barnacle Boy}`|<ins>Barnacle Boy</ins>| - |
|`\textbf{Text}`|**Write bold**|`\textbf{Man Ray}`|**Man Ray**| - |
|`\lstinline{Text}`|`Code One-Liner`|`\lstinline{Dirty Bubble}`|`Dirty Bubble`| - |
|`\^{Letter}`|Circumflex (^) above text|`\^{a}`|â| - |
|`\textsubscript{Text}`|Subscript the text|`H\textsubscript{2}O`|H<sub>2</sub>0| Nestable, you can subscript a subscript ...|
|`\textsuperscript{Text}`|Superscript the text|`Bubbly\textsuperscript{Buddy}`|Bubbly<sup>Buddy</sup>| Nestable, you can superscript a superscript ...|
|`\numprint{Number}`|Write number with 1k separators|`\numprint{4711}`|4,711| The template uses English number format |
|`\underline{Text}`|<ins>Underline text</ins>|`\underline{Barnacle Boy}`|<ins>Barnacle Boy</ins>| - |
|`\`|Escape character, if you want to use characters that are preoccupied by LaTeX, i.e. **%** |`\%`|%| - |


# 🙌🏼 Credits

For the creation of this thesis LaTeX template, the [LaTeX Master template](https://github.com/a-czyrny/LaTeX-Master-Vorlage) from [Alexander Czyrny](https://github.com/a-czyrny) was used, which is licensed under [Attribution-NonCommercial-ShareAlike 4.0 International](https://creativecommons.org/licenses/by-nc-sa/4.0?ref=chooser-v1). Furthermore, the template was translated and adjusted to own needs.

# 👩🏼‍⚖️ License

**Apache License 2.0**, aka "Just use it for whatever reason, I am happy to help. 🌝"

# ☑️ TODO
* add Cheat sheet section
* 9_misc/figures/signature.png -> add own signature
* add links to lines of code in template, add links wherever applicable
* Toogle View mode multiline tip

# ❓FAQ