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

------

## 页面

- **引入其他界面**

  ```latex
  \input{resume/education.tex}
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

  


