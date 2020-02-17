# LaTex知识点🧀️

[TOC]

------

## 矩阵

- **[方括号矩阵]**：两行三列

  ```latex
  \begin{bmatrix}1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}
  ```

- **(圆括号矩阵)**

  ```latex
  \begin{pmatrix} \end{pmatrix}
  ```
  
- **标题**

  ```latex
  \section{}					% 一级标题
  \subsection{}				% 二级标题
  \subsubsection{}		% 三级标题
  ```

- **缩进**

  ```latex
  \indent this is a text
  ```

  

------

## 页面

- **引入其他界面**

  ```latex
  \input{resume/education.tex}
  ```
  
- **目录**

  ```latex
  \tableofcontents
  ```

- **新页面**

  ```latex
  \newpage
  ```



## 段落

- **缩进**：

  - 段落自动缩进2em
  - 段落不想缩进，在开头添加`\noindent`

  ```latex
  \usepackage{indentfirst} 
  \setlength{\parindent}{2em}
  ```

- **标题**

  ```latex
  \section{This is section}
  \subsection{This is subsection}
  \subsubsection{This is subsubsection}
  ```

- **换行**：`\\`

- **粗体**：`\textbf{black text}`

- **超链接**：

  ```latex
  \usepackage[colorlinks,linkcolor=blue,urlcolor=blue]{hyperref}
  \hypersetup{colorlinks=true,citecolor=blue,linkcolor=blue,linktocpage=true}
  
  \url{http://www.caac.gov.cn/XXGK/XXGK/TJSJ/201905/t20190508_196033.html}
  ```

- **罗马数字**：`\romannumeral1`

- **标签**:

  ```latex
  % 设置标签
  \label{subsection:passenger_track}
  \label{fig:figure_1}
  
  % 引用标签
  \ref{subsection:passenger_track}
  ```

  

------

## 列表

- **有序列表**

  ```latex
  \begin{enumerate}
      \item {first item}
      \item {second item}
  \end{enumerate}
  ```

- **无序列表**

  ```latex
  \begin{itemize}
      \item {first item}
      \item {second item}
  \end{itemize}
  ```

- **罗马数字列表**

  ```latex
  \begin{enumerate}[label=(\roman*)]
      \item {first item}
      \item {second item}
  \end{enumerate}
  ```

  

------

## 公式

- **插入公式**

  ```latex
  \begin{flalign}
  \end{flalign}
  ```
  
- **连等式**（对号对齐）

  ```latex
  \begin{equation}
  \begin{aligned}
  x &= 0 \\
  &= 1 \\
  &= 2
  \end{aligned}
  \end{equation}
  ```

  

------

## 代码

- matlab代码

  ```latex
  \lstinputlisting[caption={this is a caption}]{src/test.m}
  ```

  



## 表格

- **指定宽度并居中**

  ```latex
  \usepackage{array}
  p{2cm}<{\centering}
  ```

  

```latex
\begin{table}[H]
    \centering
    \begin{tabular}{|p{5cm}|c|c|}
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

### 长表格(超过一页)

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



## 图像

- **插图中caption过长换行**：`\protect\\`
- **强制图像标题居中**：`\usepackage[justification=centering]{caption}`