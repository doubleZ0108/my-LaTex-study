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

------

## 列表

- 有序列表

  ```latex
  \begin{enumerate}
      \item {first item}
      \item {second item}
  \end{enumerate}
  ```

- 无序列表

  ```latex
  \begin{itemize}
      \item {first item}
      \item {second item}
  \end{itemize}
  ```

- 罗马数字列表

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



------

## 代码

- matlab代码

  ```latex
  \lstinputlisting[caption={this is a caption}]{src/test.m}
  ```

  