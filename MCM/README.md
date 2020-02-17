# 美赛Latex模板

[toc]

------

## 官方控制页2020

```latex
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%% MCM/ICM LaTeX Template %%
%% 2020 MCM/ICM           %%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\documentclass[12pt]{article}
\usepackage{geometry}
\geometry{left=1in,right=0.75in,top=1in,bottom=1in}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
% Replace ABCDEF in the next line with your chosen problem
% and replace 1111111 with your Team Control Number
\newcommand{\Problem}{ABCDEF}
\newcommand{\Team}{1111111}
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

\usepackage{newtxtext}
\usepackage{amsmath,amssymb,amsthm}
\usepackage{newtxmath} % must come after amsXXX

\usepackage[pdftex]{graphicx}
\usepackage{xcolor}
\usepackage{fancyhdr}
\lhead{Team \Team}
\rhead{}
\cfoot{}

\newtheorem{theorem}{Theorem}
\newtheorem{corollary}[theorem]{Corollary}
\newtheorem{lemma}[theorem]{Lemma}
\newtheorem{definition}{Definition}

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\begin{document}
\graphicspath{{.}}  % Place your graphic files in the same directory as your main document
\DeclareGraphicsExtensions{.pdf, .jpg, .tif, .png}
\thispagestyle{empty}
\vspace*{-16ex}
\centerline{\begin{tabular}{*3{c}}
	\parbox[t]{0.3\linewidth}{\begin{center}\textbf{Problem Chosen}\\ \Large \textcolor{red}{\Problem}\end{center}}
	& \parbox[t]{0.3\linewidth}{\begin{center}\textbf{2020\\ MCM/ICM\\ Summary Sheet}\end{center}}
	& \parbox[t]{0.3\linewidth}{\begin{center}\textbf{Team Control Number}\\ \Large \textcolor{red}{\Team}\end{center}}	\\
	\hline
\end{tabular}}
%%%%%%%%%%% Begin Summary %%%%%%%%%%%
% Enter your summary here replacing the (red) text
% Replace the text from here ...
\begin{center}
\textcolor{red}{%
Use this template to begin typing the first page (summary page) of your electronic report. This \newline
template uses a 12-point Times New Roman font. Submit your paper as an Adobe PDF \newline
electronic file (e.g. 1111111.pdf), typed in English, with a readable font of at least 12-point type.	\\[2ex]
Do not include the name of your school, advisor, or team members on this or any page.	\\[2ex]
Papers must be within the page limit specified in the problem statement.	\\[2ex]
Be sure to change the control number and problem choice above.	\\
You may delete these instructions as you begin to type your report here. 	\\[2ex]
\textbf{Follow us @COMAPMath on Twitter or COMAPCHINAOFFICIAL on Weibo for the \newline
most up to date contest information.}
}
\end{center}
% to here
%%%%%%%%%%% End Summary %%%%%%%%%%%

%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\clearpage
\pagestyle{fancy}
% Uncomment the next line to generate a Table of Contents
%\tableofcontents 
\newpage
\setcounter{page}{1}
\rhead{Page \thepage\ }
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
Begin your paper here


%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
\end{document}
\end
```

------

## 模块

### 目录

```latex
%---------以下生成目录----------
\tableofcontents
\thispagestyle{empty}   % 不要页眉页脚和页码
\newpage
```

### 符号表

```latex
\begin{center}
\begin{longtable}{cp{13cm}} 
\caption[Notations]{Notations}\\

\hline \hline
\multicolumn{1}{c}{\textbf{Symbol}} & \multicolumn{1}{c}{\textbf{Definition}}\\ \hline 
\endfirsthead

\multicolumn{2}{c}%
{{\bfseries \tablename\ \thetable{} -- continued from previous page}} \\
\hline \multicolumn{1}{c}{\textbf{Symbol}} &
\multicolumn{1}{c}{\textbf{Definition}} \\ \hline 
\endhead

\hline 
\centering
\multicolumn{2}{l}{{Continued on next page}} \\ \hline
\endfoot

\hline \hline
\endlastfoot

	$r$&The distance between a taxi and downtown.\\
	...\\
	$d$&The distance between the taxi and the airport. \\

\end{longtable}
\end{center}
```

### 引用

- **引用文献**

  ```latex
  $^{[\ref{ref:ref1}]}$
  $^{[\ref{ref:ref3}][\ref{ref:ref4}]}$
  ```

(不太好，现凑活用)

```latex
\begin{enumerate}[[ 1]
    \item \label{ref:ref1}
    ] Liu junjuan, wang wei, xiao meidan. Study on traffic density and speed model in single-center city [J]. Journal of railway science and engineering,2011,8(01):113-117.
    \item \label{ref:ref2}
    ] Anonymity. Shanghai taxi GPS data sets [DB/OL]. \\
\end{enumerate}
```

### 公式

```latex
\begin{equation}
    e^{i\theta}=\cos\theta+i\sin\theta.
\end{equation}
```

### 图像

- **单个图像**

  ```latex
  \begin{figure}[H]
      \centering
      \includegraphics[width=0.5\textwidth]{figure/figure_1.png}
      \caption{Number of people waiting in "boarding area" - time chart}
      \label{fig:figure_1}
  \end{figure}
  ```

- **两个图像并排**

  ```latex
  \begin{figure}[H]
  \subfigure{
      \begin{minipage}[t]{0.4\textwidth}
      \centering
      \includegraphics[width=\textwidth]{figure/figure_9_1.png}
      \end{minipage}
  }
  \subfigure{
      \begin{minipage}[t]{0.4\textwidth}
      \centering
      \includegraphics[width=\textwidth]{figure/figure_9_2.png}
      \end{minipage}
  }
  \caption{Model of airport queuing distance to carry passengers - operating time}
  \label{fig:figure4}
  \end{figure}
  ```

### 表格

```latex
\begin{table}[H]
    \centering
    \begin{tabular}{|p{5cm}<{\centering}|c|c|}
        \hline
        Data description & Symbol & The numerical\\
        \hline
        The distance from the airport to the center as the crow flies & $r$ &50\\
        \hline
    \end{tabular}
    \caption{Traffic data of Shanghai}
    \label{tab:traffic_data}
\end{table}
```

- **表格中有图片**

  ```latex
  \begin{table}[H]
      \centering
      \begin{tabular}{|p{4cm}|p{3cm}|p{3cm}|p{2cm}|p{3cm}|}
          \hline
           Travel purpose & graphic\\
           \hline
          The movement of a position between two points for the purpose of &  \begin{minipage}{0.1\textwidth}\includegraphics{figure/table_5_figure_1.png}\end{minipage}\\ 
          \hline
          Movement with other behavioral goals & \begin{minipage}{0.1\textwidth}\includegraphics{figure/table_5_figure_2.png}\end{minipage}\\
          \hline
      \end{tabular}
      \caption{Three types of typical walking purposes and walking characteristics}
      \label{tab:three_type}
  \end{table}
  ```

  

