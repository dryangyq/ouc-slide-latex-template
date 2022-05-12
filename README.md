# 中国海洋大学演示文稿Latex模板

中国海洋大学演示文稿Latex非官方模板。

本模板修改自[HelmholtzAI](https://github.com/Helmholtz-AI-Energy/beamer-template)模板。在原有模板基础上进行了大量修改。

模板主要使用海大公布的标准色，包括海大蓝、海大天蓝、海大红、樱缤粉、文脉棕、专金、专银。

此外，使用了大量的信息框来增加模板的活力。

# 文件结构

模板中的文件主要包括:

1. slide.tex：主文件，编写的演示文稿内容主要存放在该文件当中。
2. oucslide.sty：模板的样式文件。
3. font:字体文件夹，所有编译需要用到的字体。默认字体使用的是华为鸿蒙字体。
4. theme:主题文件夹。
    1. beamercolorthemeOUCSlide.sty：颜色定义文件。
    2. beamerfontthemeOUCSlide.sty：字体定义文件。
    3. beamerinnerthemeOUCSlide.sty：内部元素定义文件。
    4. beamerouterthemeOUCSlide.sty：整体布局定义文件。
    5. beamerthemeOUCSlide.sty：主题定义文件。
5. logos：模板中使用的Logo存放文件夹。
6. figs：插入的图片文件夹。
7. fontawesome.pdf：图标使用说明文件。

# 使用方法
1. 从git上clone项目到本地。目前，共有3个git库供选择，分别是：[Github](https://github.com/dryangyq/ouc-slide-latex-template.git)、[Gitee](https://gitee.com/dryangyq/ouc-slide-latex-template.git)和[Gitlab](https://gitlab.com/dryangyq/ouc-slide-latex-template.git)。这三个库都和[源库](https://git.yangyq.net/laoyang/ouc-slide-latex-template.git)保持一致和同步，从理论上来讲，使用任何一个库都可以。
2. 安装Tex编译器，推荐使用[TexLive](https://tug.org/texlive/)，安装成功后，可以使用自带的TeXworks打开目录下的tex文件进行编译。
3. 可以安装其他的IDE工具进行Tex文件的编写和修改，推荐使用[Visual Studio Code](https://code.visualstudio.com/)。
4. 编译时，请选择XeLaTex，有时候，可能需要连续编译两次，以得到正确的页码和图表编号。

# 元素介绍
## 使用分节

本模板使用分节进行整体规划，章节共三级，对应的关键字分别是：
```
\section
\subsection
\subsubsection
```
其中，\section会有单独的页面进行显示。如下图所示。而且，section将会出现在目录页面中。
![section](/figs/fig01.png )
\subsection 和 \subsubsection都没有单独的页面想对应，他们会出现在对应章节的frame中，作为标题进行呈现，并且加入了自动编号的效果。需要说明的是，\subsection是必须的，而 \subsubsection 却可有可无。他们呈现出的最终的效果，如下图所示。
![subsection](/figs/fig02.png)
需要注意的是，虽然frame的标题，是由subsection和subsubsection自动生成的，但是frame中的frametitle仍然是必须的，否则没有frametitle这个元素，标题无法自动填充。