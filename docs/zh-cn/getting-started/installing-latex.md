# 安装LaTeX

Zettlr支持导出多种文件格式，包括PDF。导出PDF有两种方式：通过Zettlr自带的导出功能和借助外部程序LaTeX。Zettlr自带的导出格式是`Simple PDF`，这先是以HTML格式导出，然后类似于浏览器打印网页一样"打印"出文件。

要导出更高级的PDF文件，您需要安装[LaTeX](https://en.wikipedia.org/wiki/LaTeX)。LaTeX是一种排版语言，允许进行大量自定义处理，但由于它是一个相对较大的程序，没有把它打包进Zettlr。以下是安装Latex的方法。

LaTeX分发了两个版本：一个是"完整安装”，包含了用于直接编写TeX的各种图形程序，另一个是"最小化安装“，只包含了编译器。Zettlr只需要"最小化安装“（因为它只需要编译器），但如果您想更多地使用LaTeX，您可以安装完整的软件包。

!!! 注意

    如果您安装的是“最小化安装”，之后需要安装额外的包。请阅读本指南结尾处，了解如何执行此操作。

## Windows

在Windows上安装LaTeX的方式与安装任何其他程序相同。只需下载以下两个版本之一：

* 最小化安装配置：MikTeX ([下载](https://miktex.org/download))
* 完整安装配置：TeX Live ([下载](https://www.tug.org/texlive/))

## macOS

与Windows类似，macOS的安装程序也很简单，可以安装两个版本之一：

* 最小化安装配置：Basic TeX ([下载](https://www.tug.org/mactex/morepackages.html))
* 完整安装配置：MacTeX ([下载](https://www.tug.org/mactex/mactex-download.html))

## Linux

通常有多个LaTeX包可直接从Linux发行版的包管理器安装。也包括最小和完整版本的包。下面列出了常见Linux发行版上的安装方式。

!!! 注意

    安装哪个版本其实无所谓，但有一个要求：您需要安装`xetex`二进制文件，因为这是Zettlr默认使用的编译器。如有疑问，请参考发行版的手册，了解如何正确安装TeX。

### Debian/Ubuntu

使用XeLaTeX编译器的最小化安装配置：

```shell
$ sudo apt install texlive-base texlive-xetex
```

完整安装配置：

```shell
$ sudo apt install texlive-full
```

### Fedora/RHEL

Fedora提供三种发布版，基础版、中间版和完整版。安装其中之一即可：

```shell
$ sudo dnf install texlive-scheme-basic
$ sudo dnf install texlive-scheme-medium
$ sudo dnf install texlive-scheme-full
```

### Flatpak

安装Flatpak的texlive插件（请注意这是完整版本，因此相当大）：

```shell
$ flatpak install org.freedesktop.Sdk.Extension.texlive
```

## 安装附加包

大多数LaTeX功能以包的形式实现。默认情况下，最小化安装只包括一组基础包。Zettlr使用的默认模板需要安装一些额外的包，但它们通常只有几千字节大小，因此不会占用太多磁盘空间。

我们建议只有当Zettlr在导出过程中出现问题时再安装包。如果您缺少某个包，Zettlr将提醒这两种错误之一：`Command \somecommand not defined`，或是`File somefile.sty not found`。

在这两种报错情况下，可能是由于某个命令或文件是由包提供。安装缺少的包的过程非常简单明了：

!!! 注意

    在 Windows 上，LaTeX将尝试自动安装缺失的包，并会询问您是否允许它这样做。

1. 所有LaTeX包都列在["Comprehensive TeX Archive Network" (CTAN)](https://www.ctan.org/)网站上。找到包的名称（包括扩展名`.sty`）或命令，并使用搜索栏进行查找。
2. 例如，如果LaTeX报告缺少 `\hypertarget` 命令，请像[这样](https://www.ctan.org/search?phrase=hypertarget)进行搜索。
3. 对于 "hypertarget"，它会返回一个包: `gmiflink`。如果有多个结果，请尝试搜索以确定需要哪个包。
4. 在macOS或Linux上，打开终端窗口，然后键入以下命令安装：`sudo tlmgr install <packagename>`。
5. 安装包后，请尝试重新导出文件。这时应该能正常导出了，否则请重复以上步骤。
