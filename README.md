# Prject Title

This is the thesis repository for the graduation project template at Qassim University. All 498 students should use this template for consistency in the outputs. As of now there are no guidelines on the changes allowed for the document theme. However, we recommend keeping it as it as (especially the configurations that helps us read and comment on the report such as the double-spaced lines).

## Files Structure

- Any file starts with a digit (e.g., `00-<name>.tex`) is one of the main document files (either the main one or one of the chapters).
- The directory [figures](figures) is where all the figures used in the document should be placed. Students are free on how the content of the figures directory is organized. 
- The file [ref.bib](ref.bib) is where all the references for the project are saved and organized.
- The file [Makefile](Makefile) is a helper file to typeset the document in a clean way (tested on MacOS and Linux only).

## Typeset Instruction

The given template has no special configurations required. Nevertheless, this section aims to help you figure out "what you need" and "what you should do" to typeset (build) this template.

### Prerequisites:

Whether you are using Windows, macOS, or Linux, you MUST have pdflatex installed. To obtain the latest pdflatex version (and more), here are some links to the widely used tex distribution for each operating system (note: you are free to use any other distribution as long as it provides pdflatex):
- Windows: MikTex (https://miktex.org/download)
- macOS: MacTex (https://tug.org/mactex/)
- Linux: Simply run `apt-get update & apt-get install texlive-full`.

Please note these are not latex editors. These are latex distributions (engines/compiler). Some of the distribution might come with a standard editor, but it is your responsibility to find one that is good for your work. 


### Build with MacOS or Linux

Assuming you installed pdflatex correctly and have all the required packages, all you need is to run the following command from the root of this project (i.e., here):

```bash
make clean all
````

The build output will be stored in a new directory named `build`. Never add the output directory to this repository. The script given is a simplification of the build process. Using the tags `clean` and `all` will typeset the document many times (to ensure all required aux files are built before generating the last version). If you are not making changes to sections (e.g., adding a new section) or introducing new references, then using `make` alone is good enough and faster.


### Build with Windows

Using your editor of choice,
1. Open the file `00-main.tex`. 
2. Make sure the typesetting engine is `PDFLaTeX` (usually it is setup by default).
3. Run the typesetter. 
4. Check for the PDF file generated in the same directory

### A Copy on Overleaf

Consult you supervisor for having a copy on Overleaf. 



## Revision History

| Name          | Date          | Change Applied  |
| ------------- |:--------------|:----------------|
| Dina Ibrahim  | NA            | Established the template with all the essential sections and cover pages  |
| Ziyad Alsaeed | Sep 9, 2022   | <ul><li>Add all the file we should ignore to .gitignore</li><li>Reorganized the files structure to have the main files in the root and other (e.g., figures) have their own directories. The new structure is better as it will make the document compatible with all different OSs or online editors.</li><li>Fixed all the references to in the main files to adhere to the new structure.</li><li>Introduced a Makefile for unix based OSs. The make file provides a cleaner build and faster for repetition.</li><li>Changed the spacing in the document to be double-spaced. This is a common setup to use with report. Also, it is easier on the eyes for professors as well as it allows space for annotations.</li></ul> |
| Ziyad Alsaeed | Sep 11, 2022  | <ul><li>Removed the Arabic handling packages (e.g., `fontspec` and `bidi`) and substituted them with a pre-defined PDF header. This method will safe us from the headache of deadline with the left-to-right and right-to-left text as well as it grantees the resolution of the header will be sustained.</li><li>Updated the build script (Makefile) to use `pdflatex` instead of `xelatex`. This is only possible after making the fix above. The goal is to make it easier to typeset the document across different platforms. If a group chooses to introduce some Arabic text it is their responsibility to make the necessary changes.</li><li>Introduced this README file to explain all the essential elements of using this template and keep track of major changes.</li><li>4</li></ul> |