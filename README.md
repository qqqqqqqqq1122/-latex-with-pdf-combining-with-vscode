# -latex-with-pdf-combining-with-vscode
真正的实现实时联动“所见即所得”latex with pdf“
作者：mathlab
链接：https://zhuanlan.zhihu.com/p/3574614730
来源：知乎
著作权归作者所有。商业转载请联系作者获得授权，非商业转载请注明出处。

为了用BaKoMa TeX Word预览，必须在文档导言处使用\input preamble.tex，完全是SWP 5.5的局限性及BaKoMa TeX的需求所致。如果单独使用SWP 5.5 Tectonic的话，则可直接使用CTeX文档类了。如果你是键盘输入高手，且熟悉LaTeX的相关命令，则可选择VsCode + BaKoMa TeX Mini组件，完全可以作为LaTeX的专业级工具。这里也有两种选择：用VsCode新建或打开LaTeX文档，VsCode会自动保存文档。当新建的文档具有完整的导言、开始与结束语句后，单击右上第一个三角按钮，Tectonic会编译XeLaTeX文档为PDF文件。单击右上角第一个窗口按钮，按n，则会启动SumatraPDF预览PDF文件。在VsCode中输入、编辑，SumatraPDF会即时更新PDF文件。如果单击右上角第一个窗口按钮，按y，则会启动BaKoMa TeX Word预览DVI文件。在VsCode中输入、编辑，BaKoMa TeX Word会几乎同时更新DVI文件。关键是在BaKoMa TeX Word也能输入、编辑，VsCode也会更新源代码。由于BaKoMa TeX使用兼容e-tex的LaTeX系统，故使用BaKoMa TeX Word预览时，在LaTeX文档的导言一开始处需加上如下5行代码：\ifdefined\XeTeXversion\else\ifdefined\pdftexversion\else
\newcount\pdftexversion\pdftexversion=140
\def\pdftexrevision{18}
\fi\fi
重新播放LaTeX专业级输入编译工具            链接：Portable_VSCode_Tectonic_BaKoMa.TeX 提取码：2024SWP 5.5&6.1及VsCode均带有Tectonic系统，可编译XeLaTeX文档，BaKoMa TeX自带LaTeX系统，用e-latex 2e模仿PDFLaTeX编译LaTeX文档，均能独立运行，但两者组合要照顾各自需求。本文应该是作为SWP及BaKoMa TeX组合的终结篇了。
