# 导入文件

如果你是从Microsoft Word或LibreOffice等文字处理程序迁移过来，你会有一些扩展名为`.docx`或`.odt`的文件，这些格式的文件包含有重要信息。但是，Zettlr是一款基于Markdown的编辑器，无法直接打开和读取这些文件。

要使这些文件可供Zettlr访问，你需要先将其导入。

过程很简单：第一步选择目标文件夹，在文件管理器中，选择要将文件导入的文件夹。第二步选择“文件”&rarr;“导入文件”，选择要导入的所有文件。Zettlr将逐个把每个文件从其原始格式转换为Markdown。

转换完成后，导入的文件会显示在所选文件夹中，你可以马上开始处理它们。

## 支持的文件类型

Zettlr使用Pandoc导入文件，因此支持多种文件格式。导入文件的要求是Pandoc支持该文件格式，并且能够将其转换为Markdown文件。

！！！注意：
    你的计算机可能没有显示部分或全部的文件扩展名。你可以更改文件浏览器设置以显示所有文件扩展名。

Zettlr根据文件扩展名识别文件类型并选择适当的导入方法。以下是当前支持的文件类型扩展名的列表：

| 文件扩展名      | 描述                            |
|----------------------|----------------------------------------|
| `*.md`, `*.markdown` | Markdown文档                     |
| `*.rmd`              | RMarkdown文件                        |
| `*.mdx`              | 含JSX的Markdown文件                |
| `*.docx`, `*.doc`    | Microsoft Word文档               |
| `*.odt`              | OpenDocument文件                     |
| `*.rtf`              | 富文本文档（Rich-Text Format）             |
| `*.html`, `*.htm`    | HTML文档                         |
| `*.tex`, `*.latex`   | LaTeX文档                        |
| `*.epub`, `*.fb2`    | 电子书文件（E-book）                           |
| `*.wiki`             | 各种Wiki-formats (MediaWiki, etc.) |
| `*.org`              | ORGmode文档                      |
| `*.rst`              | reStructuredText文档             |
| `*.docbook`          | DocBook文件                          |
| `*.textile`          | Textile文档                      |
| `*.t2t`              | txt2tags文档                     |
| `*.muse`             | Muse文档                         |
| `*.opml`             | OPML大纲文档                 |
| `*.haddock`, `*.hs`  | Haskell source code文档      |
| `*.roff`, `*.ms`     | 各种"man pages"格式            |
| `*.csv`              | 逗号分隔列表（Comma-Separated lists）                  |
| `*.ipynb`            | Jupyter Notebook文档             |
| `*.jira`             | Jira issues                            |

!!! 注意

    Zettlr会自动查找适用于特定文件格式读取器的第一个导入配置文件（import profile）。因此，如果你下载了支持同一个读取器的多个Pandoc配置文件，请注意配置文件的排列顺序。

## 与同事合作

当与重度使用Word的同事协作时，文件转换过程同样能发挥用途。你可以将Markdown文件导出为`.docx`格式分享给同事（例如请他们批注评论）。他们反馈了修改后的文件后，你可以将其重新导入Zettlr。

你可以通过修改导入配置文件来优化导入器的工作方式。例如，默认情况下，Zettlr会指示Pandoc从 Word文档中提取图像和其他媒体文件并将它们存储在资源目录中以保留这些媒体文件。

了解如何修改导入配置文件，请参阅[默认文件的文档](../advanced/defaults-files.md)。
