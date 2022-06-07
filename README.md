### Latexmk命令
如果你还不了解 Latexmk 是什么东东，这里简单的介绍一下：LaTeX 要生成最终的 PDF 文档，如果含有交叉引用、BibTeX、术语表等等，通常需要多次编译才行。而使用 Latexmk 则只需运行一次，它会自动帮你做好其它所有事情。通常情况下，你安装的 LaTeX 发行版已经包含了 Latexmk，我们并不需要手动安装它。

### xelatex 命令行
最简单的命令
```
xelatex a.tex
```

但这个命令遇到错误不会停止，你必须不断的按回车键才行。

以下是几个比较常用的命令
- -halt-on-error 和 -interaction=nonstopmode 参数 使编译遇到错误时立即停止
- -file-line-error 使报错输出文件和行号
- -synctex=1 则开启 synctex 的功能

### latexmk 结合 xelatex 编译
`latexmk -xelatex -file-line-error -halt-on-error -interaction=nonstopmode -synctex=1  a.tex`
