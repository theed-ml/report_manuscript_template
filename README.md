# Report Manuscript Template

## 1. Purpose

The purpose of a report template is to provide a consistent format for writting project's reports. I strongly encourages the use of the report manuscript template provided in this repository.

## 2. Structure

The report manuscript has the following structure:

- Title page
- Table of Contents
- Table of Figures
- Table of Abbreviations
- Abstract
- 1.Introduction
- 2.Background
- 3.Proposed Approach
- 4.Specification & Design
- 5.Implementation
- 6.Results & Evaluation
    * 6.1.Methodology
    * 6.2.Data set
    * 6.3.Results & Data Analysis
    * 6.4.Discussion
- 7.Future Work
- 8.Conclusions
- 9.References

## 3. Using the template

* There is a TeX file for each chapter
* Chapters files are placed under the directory _chapters_ and they are included in the report 
* **Figures** must be placed into the directory _figures_. It means that this is the directory where LaTeX will look for the graphics.
* Author's name and affiliation must be changed in the **report.tex** file
* Bib entries must be defined in the **references.bib** file.

### 3.1. Generating the report

Open the file **report.tex** and compile it. This can be also done through the available _Makefile_. 

### 3.2. LaTeX writing tips

* In your LaTeX document, avoid as much as possible to control the layout. Hence, you should never use ``\\`` either you want to start a new paragraph or you don't but you should let LaTeX format the paper.
* Figures and tables are usually either placed on top or on bottom of the page, rarely in the middle. In other words, you should not force LaTeX to place figures or tables where you would like to see them.
* Tables' captions are placed above the table.
* Figures' captions are placed under the figure.
* Tables should only have ``\toprule``, ``\midrule``, and ``\bottomrule``. For instance:

```
   \begin{table}
     \centering 
     \caption{Defining a table in \LaTeX{}}\label{tb:example} 
     \begin{tabular}{rl}    
       \toprule
       \textbf{Column 1} & \textbf{Column 2} \\ 
       \midrule
       A & 42\\
       B & 7\\
       C & 707\\
       \bottomrule
     \end{tabular}
   \end{table}
```

* You can use [Table Generator](https://www.tablesgenerator.com) to help you design your tables.
* Always provide a label for your sections, figures, tables, and listings. 
* It's a good practice to prefix your labels using the prefixes, __fig:__, __sec:__, __tb:__. This will be useful when an auto-complete suggests several entries and you need to select the one you want.
* Use ``\Cref`` to reference to figure, table, section, or listing. Thus, instead of writing for instance: ``as can be seen in Figure 1``, you write: ``as can be seen in~\Cref{fig:sample}``. 
* Use ``~`` to put a space between a word and a reference or citation; e.g., ``in~\cite{}``. 
* Use ``\eg{}`` to write e.g., and ``\ie{}`` to write i.e., in your text. 
* Don't describe any acronym in your text. Instead, use ``\gls{your-acronym}``and put its definition in the _abbreviations.tex_ file. For example 

% in the acronym file

```
\newacronym{ai}{AI}{Artificial Intelligence}
```

% in your text

```
\gls{ai} ... 
```

* Use ``\(\)`` or ``\[ \]`` to write math expressions
* Don't include neither the path nor the extension of the figure, when including one. 
* Set equations, floats, and any other environments with commented blank lines. For example: use ``\citeauthor{somebibentry}`` to include authors' names in the text.

## 4. References

* D. Verna, *[Towards LATEX coding standards](http://www.tug.org/TUGboat/tb32-3/tb102verna.pdf),* TUGboat, vol. 32, no. 3, pp. 309–328, 2011.