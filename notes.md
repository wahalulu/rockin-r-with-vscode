
## Why

- multiple languages {{< fa brands r-project >}}, {{< fa brands python >}}
- remote compute w/o having to configure server
- extensions
- 

::: notes
-   Most data professionals are typically not trained as developers/engineers but need to think like one
-   These ideas will make you a better programmer
-   Many years coding R and Python
-   Aspiring to be a better programmer
-   Interacting with large scale and distributed systems
-   Crappy code in the wild
:::

## Aargh

This is some text

::: notes
thigs that frustrate
:::

## My VSCode Settings

```json
{
    ...
    "editor.fontSize": 14,
    "editor.fontFamily": "Fira Code",
    "terminal.integrated.fontSize": 14,
    "terminal.integrated.fontFamily": "Fira Code",
    "editor.fontLigatures": true,
    "r.plot.useHttpgd": true,
    // https://stackoverflow.com/questions/57395681/getting-visual-studio-code-to-auto-format-r-code
    "[r]": {
        "editor.formatOnType": true,
        "editor.formatOnSave": true,
//        "editor.defaultFormatter": "REditorSupport.r"
    },
    "r.sessionWatcher": true,
    //"r.bracketedPaste": true,
    //"r.rterm.mac": "/Users/marck/miniforge3/bin/radian",
    "r.rterm.option": [
        "--no-save",
        "--no-restore",
        "--no-restore-history",
        "--no-site-file",
        "--quiet"
    ],
    ...
}

## My VSCode Keybindings


```json
[
  {
    "key": "alt+-",
    "command": "type",
    "when": "editorLangId =~ /r|rmd|qmd/ && editorTextFocus",
    "args": {
      "text": " <- "
    }
  },
  {
    "key": "ctrl+shift+m",
    "command": "type",
    "when": "editorLangId =~ /r|rmd|qmd/ && editorTextFocus",
    "args": {
      "text": " |> "
    }
  },
// https://stackoverflow.com/questions/71608612/how-to-add-keybindings-in-visual-studio-code-for-the-r-terminal
  {
    "key": "ctrl+shift+m",
    "command": "workbench.action.terminal.sendSequence",
    "args": { "text": " |> " },
    "when": "terminalFocus"
  },
  {
    "key": "alt+-",
    "command": "workbench.action.terminal.sendSequence",
    "args": { "text": " <- " },
    "when": "terminalFocus"
  },
]

```


## Show of hands

> -   Have you ever written an R script to be run in a non-interactive way?
> -   Did it work the first time as planned?
> -   Have you ever scheduled an R script to run without human intervention?
> -   Do you have any R script running in production?

## We're baaaack! {background-color="black" background-image="img/dancing.gif"}

## 

-   Sr.
    Cloud Solutions Architect, Microsoft

    -   6 mos as PM Azure Machine Learning

-   Adjunct Professor, Georgetown Masters of Data Science and Analytics

-   Co-Founder of DataCommunityDC

**Disclaimer:** the opinions expressed in this talk are personal and not reflective of any organization I am affiliated with.


## References

-   Plachta, Michal. *Grokking Functional Programming*, 1st ed, Manning, 2022
-   https://learn.microsoft.com/en-us/azure/architecture/example-scenario/mlops/mlops-technical-paper
-   https://daroczig.github.io/talks/
-   https://adv-r.hadley.nz/





# Thank You

marck.vaisman\@microsoft.com

## Bing
Sure, here's an expanded version of the slide content:
- Title Slide: Introduction to R in VSCode
    - Welcome to the presentation
    - Brief introduction about the presenter and the topic
- Slide 2: Overview of R
    - Definition of R
    - Use cases and industries where R is commonly used
- Slide 3: Introduction to VSCode
    - Brief history and purpose of VSCode
    - Popularity and community support
    - ## Bing
Here are some key points about the history of Visual Studio Code (VSCode):
- VSCode was first announced on April 29, 2015, by Microsoft at the 2015 Build conference.
- A preview build of VSCode was released shortly after the announcement.
- On November 18, 2015, the source of VSCode was released under the MIT License and made available on GitHub.
- Extension support for VSCode was also announced at the same time.
- On April 14, 2016, VSCode graduated from the public preview stage and was officially released to the Web.
- Most of VSCode's source code is available on GitHub under the permissive MIT License.
- The binary releases by Microsoft are freeware and include proprietary code.
- A community distribution, called VSCodium, is maintained, which provides MIT licensed binaries.

- Slide 4: Benefits of using R in VSCode
    - Explanation of the benefits like IntelliSense, debugging, etc.

VSCode extensions are primarily written in TypeScript. However, since VSCode is built with Electron, you can write an extension in JavaScript, or anything that can be transpiled to JavaScript, such as TypeScript. For example, the HTML Language Client and PHP Language Client are normal VSCode extensions written in TypeScript.


- Slide 5: Installing VSCode
    - Step-by-step guide on how to install VSCode
- Slide 6: Adding R support in VSCode
    - How to search for extensions in VSCode
- Slide 7: Searching for R Language extensions
    - Demonstration of searching for R extensions
- Slide 8: Installing the R Extension for VSCode
    - Step-by-step guide on how to install the R extension
- Slide 9: Configuring and running the R extension
    - How to configure settings for the R extension
    - Demonstration of running a simple R script
- Slide 10: Installing the R LSP Client extension
    - Purpose of the R LSP Client extension
    - Guide on how to install it
- Slide 11: Installing the languageserver package
    - Explanation of what the languageserver package does
    - Guide on how to install it
- Slide 12: Features of the languageserver package
    - Detailed explanation of the features provided by languageserver
- Slide 13: Using code snippets in VSCode
    - Explanation and demonstration of code snippets feature
- Slide 14: Previewing R graphics in VSCode
    - How to generate and preview graphics using R in VSCode
- Slide 15: Debugging features in VSCode
    - Overview of debugging features available in VSCode for R
- Slide 16: Working with folders in VSCode
    - How to organize your R scripts using folders in VSCode
- Slide 17: Additional tips for optimizing the R experience in VSCode
    - Miscellaneous tips and tricks for a smoother experience
- Slide 18: Using the radian terminal with R in VSCode
    - Introduction to radian terminal and its benefits
- Slide 19: Enabling r.bracketedPaste for using Radian
    - How to enable r.bracketedPaste and why it's useful with radian terminal
- Conclusion Slide: Recap and Q&A
    - Recap of key points covered in the presentation
    - Open floor for questions and answers


The languageserver package is an implementation of the Language Server Protocol for R. It includes features that we need to work efficiently, including auto-complete, definition provider, code formatting, code linting, information on functions on hover, color provider, and code sections. The Language Server Protocol is used by an editor client to integrate features like auto completion. The languageserver package is released on CRAN and can be easily installed.
