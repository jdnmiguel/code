# Latex-to-Word
Using Latex is extremely convenient for academic writting for several reasons, however it might happen that we need a Word version of a Latex project. The objective of this post is to provide an easy way to translate a .tex file into a .docx. 

## 1. Installing Pandoc

1. Make sure to have a Latex compiler installed. I am using [Texmaker](https://www.xm1math.net/texmaker/).
2. Open a command prompt (CMD) command: search for CMD in your terminal and open it as admin.
3. Install [chocolatery](https://chocolatey.org/install) by running the following command into the cmd
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

## 2. Comppiling your .Tex file as a .docx file.
1. Specify the folder where your .tex file is located. Be sure that the .tex file can be run properly with your Latex compiler.
``` 
cd "C:\Users\Awesome_paper"
```

2. Compile your existing .Tex file into a newly created Word document
 ```
 pandoc text.tex -o text.docx
 ```
 with 
- pandoc: command tool
- tex.tex: file name in LaTex format
- -o : output to a file
- text.docx:  file name in MS Word format

3. Cross-reference
To keep your references (e.g., table, figure, bibliography) during the conversion, a filter named pandoc-crossref has to be used. Download it [here](https://github.com/lierdakil/pandoc-crossref/releases/tag/v0.3.4.0c) and follows the installation instructions. *Note: crossref.exe has to be in the same folder as pandoc.exe*
```
pandoc text.tex –filter pandoc-crossref –bibliography=refs.bib  -o text.docx
```
