# 安装

Zettlr的安装非常简单，只需点击几下即可完成。Zettlr兼容多种平台，因此适用于大多数计算机。Zettlr为macOS、Windows和其他多种Linux系统提供了预构建程序（pre-built）。

## 最低系统要求

系统资源普适性是Zettlr的目标，但仍然需要满足一些最低要求。

* 操作系统:
    * Windows 10或更高版本
    * macOS 11.6.0或更高版本
    * Debian 8或更高版本
    * Ubuntu 12.04或更高版本
    * Fedora 24或更高版本
    * Arch Linux
    * 任何由AppImages或Flatpack支持的发行版
* 处理器: 1GHz双核64位Intel或更高配置（暂不支持32位）
    * Linux上，支持与上述相同配置的64位ARM处理器
    * macOS上，支持Apple Silicon（M1、M2等）
* 内存（RAM）：1GB
* 磁盘空间(Disk Space)：至少500MB的空闲磁盘空间

!!! 注意

请注意受支持的操作系统版本可能随时变化。受支持平台的最新列表可以在[此处](https://www.electronjs.org/docs/latest/development/build-instructions-gn#platform-prerequisites)找到。

## 安装Zettlr

### Windows

在Windows上安装Zettlr，请从[下载页面](https://www.zettlr.com/download)下载应用程序，然后双击打开安装包。默认设置下，在安装过程中会请求管理员权限，为计算机所有用户安装应用程序。

如果你没有该计算机的管理员权限，或者不想为所有用户安装，你可以选择仅为当前用户安装。这不要求管理员权限，但可能无法正常使用某些功能。

!!! 注意

    我们建议选择为所有用户安装Zettlr。

### macOS

在macOS上安装Zettlr，请从我们的[下载页面](https://www.zettlr.com/download)下载DMG文件，并双击挂载它。然后，将Zettlr图标拖动到“应用程序（Applications）”目录中，等待应用程序复制完成。

!!! 注意

    你也可通过[Homebrew](https://brew.sh/)安装Zettlr，只需运行以下命令：

    `$ brew install --cask zettlr`

    有关更多信息，请访问[Zettlr Homebrew页面](https://formulae.brew.sh/cask/zettlr)。

### Ubuntu/Debian

在Ubuntu或Debian衍生版本上安装Zettlr，请从我们的[下载页面](https://www.zettlr.com/download)下载`deb`软件包，并运行该文件。

### Fedora

在Fedora或Red Hat衍生版本上安装Zettlr，请从我们的[下载页面](https://www.zettlr.com/download)下载`rpm`软件包，并运行该文件。

### Arch Linux

得益于社区的工作，Zettlr在Arch Linux上能作为常规软件包使用。在Arch上安装Zettlr，按照Arch软件包的常规安装说明进行操作即可。更多信息请查阅[Zettlr Arch Wiki页面](https://wiki.archlinux.org/title/Zettlr)。

!!! 注意

    我们尚未收到任何有关Zettlr Arch软件包的投诉，因此认为它安全可靠。然而，由于我们没有控制软件包的编译过程，于是在此做出免责声明，表示我们不对这些软件包负任何责任。如果出现问题，请直接与软件包维护人员联系。

### AppImage

在Linux中运行AppImage格式的Zettlr。请从我们的[下载页面](https://www.zettlr.com/download)下载AppImage格式包。安装AppImage格式包的方式是，将文件放入你选择的目录中，给予运行权限，然后就可开始使用它。

### Flatpack

Zettlr也有Flatpack版本。要安装Flatpack版本，请从[Zettlr's FlatHub页面](https://flathub.org/apps/details/com.zettlr.Zettlr)下载，并按照设置说明进行设置。

!!! 注意

    Flatpack默认情况下无法访问你的文件系统。要为其提供访问权限，你必须首先使用类似[Flatseal](https://flathub.org/apps/details/com.github.tchx84.Flatseal)的软件包进行配置。如果出现问题，请在[相应的GitHub仓库](https://github.com/flathub/com.zettlr.Zettlr)联系Flatpack维护人员。请不要在主仓库（main repository）上提交报告，我们无法帮到你。

## 更新Zettlr

每次启动应用程序时，都会检查是否有更新。你还可以通过单击“帮助（Help）” &rarr; “检查更新（Check for updates）”手动更新。如果有新版本可用，Zettlr会在工具栏中显示一个“下载”图标，单击它后Zettlr会打开一个对话框，其中包含新版本编号、当前版本和更新日志，更新日志记录了新版本所有功能和bug修复。

!!! 警告

    **永远不要“跳过”版本！**我们有时会在某次更新中更改Zettlr的配置。如果你“跳过”了帮助迁移配置的必要中间版本，可能会导致更新期间数据损坏。如果你有一段时间没有更新Zettlr，请**不要**直接升级到最新版本，而是依次安装每个更新。你可以在[GitHub](https://github.com/Zettlr/Zettlr/releases)上找到所有更新的版本。

更新时请单击下载按钮，等待下载完成。然后，单击“开始更新（Begin Update）”，Zettlr将关闭并开始更新。更新程序将存放在你的下载文件夹下。更新成功后，你可以将其删除。

!!! 注意

    如果你是通过软件包管理器（例如Homebrew）安装的Zettlr，请根据你的软件包管理器的流程进行更新，以避免冲突。你可以在首选项中禁用“自动检查更新（Automatically check for updates）”设置，以防止Zettlr自动检查更新。

更新后请**等待几分钟**，以便Zettlr启动。每次更新后，文件缓存都将被清除，Zettlr的新版本首次启动时，它必须重新创建文件缓存。你打开的文件和文件夹越多，此过程可能需要的时间就越长。如果过了一会儿还没有看到任何反应，请不要担心，在Zettlr再次扫描完你的工作区后主窗口将会打开。

如果无法自动更新，你依然可以手动更新，下载适配系统的安装包（请参见上文）。首次安装和后续更新没有区别（从技术上来说），文件都是相同的。

!!! 注意

    你可以选择安装测试版（beta releases）。如果是这样，请在设置中激活“通知我有关测试版发布”。

## 卸载Zettlr

如果你对Zettlr不满意或需要卸载它，请按照以下说明操作。

!!! 注意

    如果你是通过软件包管理器安装的Zettlr，请参阅你的软件包管理器的文档，以了解如何卸载软件，而不是按照此处的说明操作。

在Windows上，进入设置页面并按照[Microsoft的说明](https://support.microsoft.com/en-us/windows/uninstall-or-remove-apps-and-programs-in-windows-4b55f974-2cc6-2d2b-d092-5905080eaf98)进行卸载。如果要删除设置和用户数据，你可以在目录C:\Users\<your-user-name>\AppData\Roaming\Zettlr中找到它们。

在macOS上，前往“应用程序”文件夹，将“Zettlr.app”移到垃圾桶中。如果要删除设置和用户数据，你可以在目录/Users/<your-user-name>/Library/Application Support/Zettlr中找到它们。

在Linux上，卸载过程取决于你的发行版以及你如何安装该应用程序。请查阅有关如何执行此操作的手册。如果要删除设置和用户数据，你可以在目录/home/<your-user-name>/.config/Zettlr中找到它们。

!!! 注意

    Zettlr还会在你的工作区内创建所谓的“隐藏”文件，以记录你的目录设置。这些文件的名称为`.ztr-directory`。卸载Zettlr后，你可以安全地删除这些文件。

## 每日编译版（Nightly Releases）

自2.0.0以来，我们提供了每日编译版。在每周一中午（UTC）自动构建每日编译版（但有时我们会手动构建）。它们包含了代码库的最新更改，它们甚至比测试版发布更新，但这也意味着它们可能包含我们尚未发现的严重错误。

每日编译版仅适用于了解使用风险的高级用户。如果你定期对设置、写作统计和文件做备份，也许可以安全地使用这个版本。我们欢迎使用每日编译版的用户通知我们遇到的错误。

要安装每日编译版，你需要手动从https://nightly.zettlr.com/下载。你的更新程序不会提醒你有关每日编译版的更新，但由于它们每周自动构建一次，因此可以确保会有新版本。

!!! 警告

    每日编译版完全自动化，我们不保证其稳定性。通常情况下不会出现问题，但这些版本有可能损坏你的计算机。使用每日编译版意味着你对你了解这些风险表示同意。

还需注意，我们不保留历史的每日编译版。每周的每日编译版只会替换以前的版本。如果某个每日编译版无法使用，请随时通知我们，以便在我们修复了错误后手动安排新版本的构建。
