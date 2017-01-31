%!TEX encoding = UTF-8 Unicode
%!TEX TS-program = xelatex
%!BIB TS-program = biber

% paper for BeLLS
\documentclass[11pt,twoside]{article}
\input{settings} % load packages, set parameters, define commands

% use the following packages if needed (if not, you can omit loading these)
\usepackage{synttree} % for drawing syntactic trees
\branchheight{2.5em} \childsidesep{0.5em} % synttree settings
\usepackage{avm} % for drawing attribute-value matrices
%\usepackage{epstopdf} % for eps graphics
\usepackage{hyperref}
\usepackage{hyperref,xcolor} %http://ctan.org/pkg/{hyperref,xcolor}
\usepackage{makeidx}
\definecolor{winered}{rgb}{0.5,0,0}

\hypersetup{colorlinks=true,
  linkcolor=blue,
urlcolor={blue},
filecolor={blue},
citecolor={blue},
allcolors={blue}}

\author{Laurie Peeters, Sandra van der Schaaf, Dian van Rooi January 31st, 2017} % no affiliation
\title{Convergence in economic performance between European countries} % do not capitalize every open class word
\addbibresource{sample.bib} % the bib file

\hyphenation{lem-mat-iz-at-ion uni-code ADVdeg Hel-ge}
\graphicspath{{pics/}} % the pictures folder


\begin{document}
\maketitle

This paper aims to empirically compare convergence of different regions in the European Community between 1980 and 1984 and 1985 and 1989. 
Our research is loosely based on the paper of \href{http://web.b.ebscohost.com/ehost/pdfviewer/pdfviewer?sid=2b519a94-f685-4d04-8e5f-5fdb94e89ef5\%40sessionmgr101&vid=1&hid=116}{Neven and Gouyette (1995)}. 
This study, as well as ours, uses data on GDP per capita derived from the world development indicators of the \href{https://www.kaggle.com/worldbank/world-development-indicators}{World Bank}.
However, our north region will be compiled from data of The Netherlands, Germany and Finland and the south region will consist of Italy, Greece and Spain.
Also, a different model will be used to analyze the dataset.
Finally, our data analysis will be carried out in Python to report the findings in a transparent way and make it easier to verify and/or reproduce them by others.

\section{Question}

Has there been convergence between northern and southern countries in Europe between 1985 and 1989?

\subsection{Motivation}

Over the last few years, outcomes of traditional growth models have been more and more challenged by new research.
Mainly the prediction of these neoclassical models that output of different regions will converge over time towards a steady state has led to an increasing amount of criticism (\href{http://web.b.ebscohost.com/ehost/pdfviewer/pdfviewer?sid=2b519a94-f685-4d04-8e5f-5fdb94e89ef5\%40sessionmgr101&vid=1&hid=116}{Neven \& Gouyette, 1995}).
For instance, when taking into account some non-convexity in production or externalities arising from the accumulation of human capital, regional outputs per capita can in fact diverge.
Also agglomeration economies may result in centripetal forces and uneven growth patterns.
Therefore, the question arises whether traditional neoclassical models are still useful when predicting convergence and making policy related decisions.

Whether or not convergence is actually happening is of great importance for policy debates on EU's \href{http://ec.europa.eu/regional_policy/en/policy/what/investment-policy/}{Regional Policy}.
In case it turns out that there is indeed convergence, this means that neoclassical models are able to provide a decent overview of regional evolution.
According to \href{http://web.b.ebscohost.com/ehost/pdfviewer/pdfviewer?sid=2b519a94-f685-4d04-8e5f-5fdb94e89ef5\%40sessionmgr101&vid=1&hid=116}{Neven \& Gouyette (1995)}, this makes it harder for \href{http://ec.europa.eu/regional_policy/en/policy/what/investment-policy/}{Regional Policy} to justify its importance for economic efficiency.

\subsection{Method}
We used data from the dataset 'World Development Indicators' by the \href{https://www.kaggle.com/worldbank/world-development-indicators}{World Bank}. 
This dataset contains more than thousand annual indicators for economic development for many countries in the world. 
For this research we used GDP per capita (current US\$).  
We will compare the northern and southern European countries by means of estimating the coefficient of the correlation between GDP per capita (current US\$) over the period of 1980 - 1984 and the period 1985 - 1989. 

\subsection{Answer}

When we exclude Finland from our northern region, we can observe convergence between the northern (the Netherlands and Germany) and southern region (Italy, Greece and Spain) between 1985 and 1989. This convergence was not present during the period of 1980 - 1984.

\subsection{Main Assumptions}
When using an OLS regression, the following assumption are implied:
\begin{examples}
\item Linear relationship
\item Multivariate normality
\item No or little multicollinearity
\item No auto-correlation
\item Homoscedasticity
\end{examples}

\section{Importing Libraries}
To be able to run the model the following python packages were used:

\section{Model}
We use our own method to see whether there is a shift in correlation between the years of 1985 - 1989 in terms of GDP per capita (current US\$). For the estimation we use the following estimation equation:

\begin{equation}
Y = \alpha + \beta (Y_{it}) + u_{it}
\end{equation}





\section{Analysis}

As mentioned above, Python was used to analyze the data. 

\section{Results}

GRAPH 

We can see in the graph that starting from 1985 GDP per capita is increasing for every country.
It can also be seen that Germany and the Netherlands are stagnating while Italy and Spain keep increasing.
Finland and Greece seem to be an exception in their region.
GDP per capita is still increasing in Finland in 1989 and appears to be constantly stagnating in Greece.

TABLES OF OLS REGRESSIONS

\section{Conclusion}
The results show that there is indeed convergence between northern and southern countries in Europe between 1985 and 1989, however, only if Finland is excluded from the dataset. 
This could mean that the neoclassical models are perfectly able to make predictions and \href{http://ec.europa.eu/regional_policy/en/policy/what/investment-policy/}{Regional Policy} 

\section{Discussion}

In 1987 the European Commission made equality one of their top priorities in its policies and started interfering more (\href{http://web.b.ebscohost.com/ehost/pdfviewer/pdfviewer?sid=2b519a94-f685-4d04-8e5f-5fdb94e89ef5\%40sessionmgr101&vid=1&hid=116}{Neven \& Gouyette, 1995}).
Unfortunately, our dataset is too short to be able to draw any conclusions on the consequences of these measures.
It will be interesting to study this in the future.
In case this research would observe a different pattern of convergence and would be able to relate this to the measures taken by the Commission, this would give an indication of the effectiveness of regional policy.

\section{References}


\	\	\ Barro, Robert J., and X. Sala-I-Martin (1990). "Economic Growth and Convergence across the United States." Working Paper 3419. Cambridge, Mass.: National Bureau of Economic Research (August). 

European Commission. (2013). Retrieved from \url{http://ec.europa.eu/regional_policy/en/policy/what/investment-policy/}
   
Neven, D., and C. Gouyette (1995). Regional convergence in the European Community. \textit{Journal of Common Market Studies}, 33(1), 47. 

World Bank. (2016). World Development Indicators. Retrieved from \url{https://www.kaggle.com/worldbank/world-development-indicators/version/1}


\section{other}
We primarily provide these guidelines and examples for producing your PDF with XeLaTeX, a modernized version of LaTeX which is compatible with Unicode and modern font handling.
XeLaTeX is included in current LaTeX distributions.
As a convenient starting point for writing, you may consider editing the template \emph{bellstemplate.tex}, which has the same settings as these guidelines.

If you cannot write your paper in XeLaTeX or otherwise produce the PDF according to these guidelines, please contact the volume editors and we will find a good solution for how your paper can be delivered.

\subsection{XeLaTeX and Unicode}\label{fontexamples}

When you write your source in Unicode, special symbols such as those in the sequence “ɐ→ə” can be typed directly in the text instead of being specified by special commands, as long as the chosen font contains the necessary glyphs.
Of course this presupposes that the font of the editor in which you write your source code also has the necessary glyphs.

Examples \refp{english}–\refp{greek}, taken from the Universal Declaration of Human Rights,\footnote{\url{http://www.ohchr.org/EN/UDHR/Pages/SearchByLang.aspx}} show sentences in different alphabets that were entered in Unicode.

\begin{examples}
 \item\label{english} All human beings are born free and equal in dignity and rights. (English)
 \item Hver maður er borinn frjáls og jafn öðrum að virðingu og réttindum. (Icelandic)
 \item Все люди рождаются свободными и равными в своем достоинстве и 
правах. (Russian)
 \item Tất cả mọi người sinh ra đều được tự do và bình đẳng về nhân phẩm và 
quyền lợi. (Vietnamese)
 \item\label{greek} Ὅλοι οἱ ἄνθρωποι γεννιοῦνται ἐλεύθεροι καὶ ἴσοι στὴν ἀξιοπρέπεια 
καὶ τὰ δικαιώματα. (Greek)
\end{examples}

\subsection{Other fonts and symbols}\label{otherfonts}

Sometimes a change of font or of font characteristics may be necessary in order to use specific alphabets, for example, Chinese, or special glyph shapes, for example Fraktur.
The \emph{fontspec} command and related commands may be used to change fonts or font characteristics.

In addition to typing Unicode characters directly in the source code, it is possible in XeLaTeX to use combinations of simple characters, such as two hyphens for an en dash -- and three hyphens for an em dash ---, and one can also use commands such as \verb!$\rightarrow$! for a right arrow $\rightarrow$.

\section{Numbered elements}

\subsection{Glossed linguistic examples and equations}

Linguistic examples are numbered continuously throughout the paper.
As usual, the numbers are in parentheses and are placed at the left margin.
It is recommended to use automatic numbering and to refer to examples by means of labels in the source code which are automatically converted to the correct numbers.
This document and the template use the \emph{covington} package which takes care of this.

Some numbered examples and references to these were already given in Section \ref{fontexamples}.
All linguistic examples in a language other than the main language of the paper need glosses (word by word translations) and an idiomatic translation.
Example \refp{dutch} illustrates the use of glosses, which are automatically aligned underneath the respective words on the first line.
Please adhere to the Leipzig Glossing Rules.
The line with glosses does not have punctuation.
An idiomatic translation is given on the third line.
This translation must be enclosed in single quotes.

\begin{example} \label{dutch}
\gll Dit is een Nederlands voorbeeld-je.
This is a Dutch example-DIM
\glt `This is a small Dutch example.' \glend
\end{example}

Linguistic rules are numbered in the same way as examples and have the same counter.
This is illustrated in rules \refp{ex:mweiness:NP-rule} and \refp{ex:mweiness:furule}.
If tabular alignment is necessary to format a rule, as in example \refp{ex:mweiness:furule}, the \emph{tabular} environment should be embedded in an \emph{extab} command in order to achieve proper alignment of the rule number.

\begin{examples} 
 \item \label{ex:mweiness:NP-rule} NP $\rightarrow$ N: $\uparrow$=$\downarrow$ \\

 \item \label{ex:mweiness:furule}
  \extab{\begin{tabular}{lll}
   IP $\rightarrow$ &  XP: & ($\uparrow$ TOPIC)=$\downarrow$\\
   & & ($\uparrow$ \{COMP | XCOMP\}* \{SUBJ | OBJ | OBL-TH\})=$\downarrow$\\
   & [\dots]
   \end{tabular}}
\end{examples}

In contrast to linguistic examples, mathematical formulas such as equation \refp{eq:prob} are by default numbered at the right margin, but they use the same counter.

\begin{equation} \label{eq:prob}
P(n_1, n_2) =  \sum_{i=0}^{N} F_{subj} + \sqrt{Z}
\end{equation}

When referring to examples and equations which have numbers in parentheses, the reference should also put the number in parentheses.
The command \emph{refp} can be used instead of \emph{ref} to achieve this.

\subsection{Tables and figures}

Tables and figures each have their own counter.
They float to where there is enough space in the document.
Numerical data should be right aligned in their column, as in Table~\ref{table}.
The simplest way of working is sometimes to let other programs (for instance R using the \emph{xtable} library) generate the correct LaTeX code for tables and to import the resulting code in your document.

\begin{table}[htbp]
 \centering
  \begin{tabular}{lcr} \hline % left aligned, centered, right aligned
      left-aligned & centered & right-aligned\\ \hline
      First row & A & 10 \\
      Second row & B & 17\\
      Third row & C & 800\\ 
      Fourth row & D & 1630\\ \hline
  \end{tabular}
  \caption{A table with different alignments of rows} \label{table}
\end{table}

Linguistic trees, diagrams, other drawings, screenshots and photographs must be treated as figures.
Like tables, they float to where there is enough space.
Do not worry too much about the exact placement of figures until the final version of your paper.

The tree structure in Figure~\ref{synttree} is drawn by the \emph{synttree} package from labeled bracketing, a process which is preferable to drawing trees by hand.
There are several similar packages with various possibilities.
Sometimes, however, it is more convenient to insert syntactic structures as screenshots.

\begin{figure}[htbp] % place here or at top or bottom or on separate page
\centering
\synttree{5}
[A [B [C [.x Some terminals]]] [D [t] [E [another] [F [terminal]]]]]
\caption{An example tree drawn from labeled bracketing using the \emph{synttree} package} \label{synttree}
\end{figure}

Picture files containing, for example, screenshots, drawings and photos can be included with the \emph{graphicx} package.
The structures in Figure~\ref{screenshots} are imported screenshots. 
Try to match the font size in screen shots somewhat to the font size of normal text.
Captions of tables and figures are not terminated by periods.
Capitalize “Table”, “Figure” and “Section” when referring to these with numbers.

\begin{figure}[htbp]
\centering
\includegraphics[width=0.34\textwidth]{c-structure.png} 
\includegraphics[width=0.65\textwidth]{f-structure.png}
\caption{C-structure and f-structure from screenshots}\label{screenshots}
\end{figure}

Diagrams such as attribute-value matrices can also be drawn in LaTeX with the help of the \emph{avm} package, as illustrated in Figure~\ref{avm}.
This package is provided with these guidelines.

\begin{figure}
\centering
\avmoptions{active}
\begin{avm}
\{ < [ subj & \rm ‘Mary’ \\ obj & \rm ‘cat’ ] > \\
[ subj & \rm ‘Bill’ \\ obj & \rm ‘dog’ ] \}
\end{avm}
\caption{An attribute-value matrix}\label{avm}
\end{figure}

\section{Citations}

%Citations are in the author-year format in parentheses \parencite{Kopka04,Mittelbach04}.
%Citations can also be textual, as \textcite{Gries09} or \textcite{Carter97}, and may have additional references to pages \parencite[pp. 34--36]{Baldwin10}.
%The final unnumbered section of the paper is the bibliography which lists the references alphabetically by author.

Citations are in the author-year format with parentheses.
When the reference is mentioned as support for what is said in the text, it is entirely included in parentheses \parencite{Kopka04,Mittelbach04}.
There may be additional references to pages or chapters at the end of the citation \parencite[pp. 34--36]{Baldwin10} and  additional material within the parentheses before the author name \parencite[for example,][p. 292]{Rosen16lre}.
When the authors' names are used in the sentence to refer to a particular publication, the names are placed before the parentheses.
For example: As \textcite{Gries09} and \textcite[p. 3556]{Dyvik16} have shown \dots

The final unnumbered section of the paper is the bibliography, which lists the references alphabetically by author.
The bibliography style uses full names and requires that the authors are listed in your \emph{bib} file with \emph{lastname, firstname} in order to distinguish between a middle name and a last name prefix, for example, \emph{Lyse, Gunn Inger and De Smedt, Koenraad}.
The capitalization of titles should be the same as that in the original publication.
These guidelines use the \emph{biblatex} package with appropriate settings which produce the desired references automatically, assuming that the data in your \emph{bib} file is correct and complete.

\section{Final remarks}

This document was typeset with XeLaTeX as included in TeX Live 2016.
The source file inputs another file \emph{settings.tex} which loads packages, sets options and defines commands.
The settings will change slightly in the future.
In particular, the final version of \emph{settings.tex} will provide final information about the volume so as to produce complete page headers.
If you have any questions after reading this text, please contact the volume editors.
If you have suggestions for improvement, please let us know.

\printbibliography

\end{document}
