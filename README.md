# A thesis base on thuthesis

基于 [ThuThesis](https://github.com/xueruini/thuthesis) @5.4.4 修改的上海海事大学本科毕业论文模板。

样例：[main.pdf](main.pdf)

---

## SmuThesis

SmuThesis 为 **S**hanghai **M**aritime **U**niversity **Thesis** LaTeX Template 缩写。

此宏包旨在建立一个简单易用的上海海事大学本科毕业论文 LaTeX 模板。

## 下载

```sh
git clone https://github.com/YunYouJun/smuthesis.git
```

## 更新

```sh
git pull
```

## 目录

目录名称 | 描述
---|---
custom | 自定义的一些内容（包括封面、承诺书、摘要）
data | 存放引言以及正文内容（通过章节分类）
figures | 存一些你文章中用到的图片
ref/refs.blib | 参考文献
.travis.yml | Travis 持续集成文件（如果你使用 Linux ，大可参考其进行环境的配置了）
main.pdf | 示例文件
thuthesis.pdf | ThuThesis 使用说明

## 使用

> 磨刀不误砍柴工。

使用过程前期可能会花费大量时间，如果没有作好准备（能折腾的精神），可能影响到您的安排，请勿轻易使用。
当然如果成功配置完成，将不再需要频繁烦恼格式的问题。

参考文献位于 `refs.blib` 文件中，请使用文件中的样例格式进行书写。编译后，LaTex 将会在最后自动生成文章中所引用到的参考文献。
只有文章中引用过的参考文献，才会被编译显示。

目录、表格索引与插图索引均会自动生成。

### LaTex 的安装与基本使用

您可参考此文档教程。

[中文版](https://github.com/luongvo209/Begin-Latex-in-minutes/blob/master/Translation:Chinese.md)

### ThuThesis 使用

本模板基于 [ThuThesis](https://github.com/xueruini/thuthesis) 修改，其他具体使用方法可参考 ThuThesis [使用说明](thuthesis.pdf)以及[示例文档](main.pdf)。

> 本项目中包括 ThuThesis 使用说明 (thuthesis.pdf)。示例文档（main.pdf）为根据上海海事大学格式修改后的文档。

---

或[下载](https://github.com/xueruini/thuthesis/releases)模板，里面包括具体使用说明以及示例文档：

- 模板使用说明 (thuthesis.pdf)
- 示例文档 (main.pdf)

### 编辑器

推荐使用 [Visual Studio Code](https://code.visualstudio.com/) 进行编辑。

并安装插件( `Ctrl + Shift + X` )：

- LaTex Workshop
- LaTex language support

`Ctrl + Shift + B` 编译生成 `main.pdf` 文档，VS Code 保存后也会自动编译。

你可以选择 `View Latex PDF` -> `View in web browser`。

### 封面与承诺书

封面与承诺书使用学校规定样式模板，请通过 Word 编辑自定义内容 `custom/*.docx` 并转为同名 pdf。

- [封面](custom/thesis-cover.pdf)
- [承诺书](custom/thesis-commit.pdf)

## Makefile 的用法

[Makefile Usage](https://github.com/xueruini/thuthesis#makefile-usage)

```shell
make [{all|thesis|shuji|doc|clean|cleanall|distclean}] \
     [METHOD={latexmk|xelatex|pdflatex}]
```

### 目标

- `make all`       等于 `make thesis && make shuji && make doc`；
- `make cls`       生成模板文件；
- `make thesis`    生成论文 main.pdf；
- `make shuji`     生成书脊 shuji.pdf；
- `make doc`       生成使用说明书 thuthesis.pdf；
- `make clean`     删除示例文件的中间文件（不含 main.pdf）；
- `make cleanall`  删除示例文件的中间文件和 main.pdf；
- `make distclean` 删除示例文件和模板的所有中间文件和 PDF。

### 参数

- **METHOD**：指定生成 pdf 的方式，缺省采用 latexmk。
  - METHOD=latexmk  表示使用 latexmk 的方式生成 pdf（使用 xelatex）。
  - METHOD=xelatex  表示使用 xelatex 引擎编译生成 pdf；
  - METHOD=pdflatex 表示使用 pdflatex 引擎编译生成 pdf。

## After

本模板未对编译源文件进行修改，仅修改了编译后的样式文件。

如果你对 LaTex 的使用较为熟练，并有需要定制的效果，推荐直接使用 [ThuThesis](https://github.com/xueruini/thuthesis) 模板。

如果您对此有什么问题建议，可以提 ISSUE，或者 Pull Request。
