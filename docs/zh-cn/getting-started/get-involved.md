# 参与进来

你想帮助Zettlr成为更棒的应用吗? 如果是的话就太好啦！不管是想要翻译Zettlr, 还是参与应用程序的开发，你来对地方了！

## 常见资源

Zettlr有一个活跃的社区，网友们在其中为彼此提供帮助。下面列出的社区，你遇到的任何问题都可以先从那里出发探索。

* [Zettlr Discord](https://discord.com/invite/PcfS3DM9Xj)：Zettlr Discord汇集了各路Discordian（似乎没有官方名称）。
* [Zettlr subreddit](https://www.reddit.com/r/Zettlr)：Zettlr subreddit是为Reddit用户而成立的社区。
* [Mastodon官方账号](https://fosstodon.org/@zettlr)：你可以实时关注到应用程序的更新。这是我们定期发布正在做的所有事情的唯一媒介。此外，这里的大多数讨论我们都会参与，因此如果你有问题，也可直接发在这里。
* [Twitter官方账号](https://fosstodon.org/@zettlr)：与我们的Mastodon账户一样。
* [我们的YouTube频道](https://www.youtube.com/c/Zettlr)：如果你更喜欢视觉向的内容，可以在这里找到一些入门视频。请注意，该频道不定期维护，视频可能已过时。
* [GitHub Discussions](https://github.com/Zettlr/Zettlr/discussions)：“古早网上论坛”的稍微更”现代“的版本。
* [GitHub issue跟踪器](https://github.com/Zettlr/Zettlr/issues)：我们改进应用程序时投入精力最多的的地方。如果你发现bug，想提出建议或功能需求，这是最合适的地方。不过，若是涉及使用流程或新添加功能的问题，**最好先在GitHub Discussions或Discord上讨论你的想法**。

## 用户贡献

对于希望获得好看且运行良好的写作应用程序的用户，只需在使用中保持敏感，注意应用程序可能产生的任何错误，更重要的是告诉我们如何使工作流程更加高效！我们只能根据自己的工作流程来判断，因此为了使应用程序对你来说更好，我们需要知道如何操作。请记住：我们无法做到把理想的工作流程原封不动地嵌入到设计中，不得不在现有工作流程和新的提议之间做出权衡，只要这两者之间做出让步的损失在可接受范围，我们将尽最大努力使功能更易于使用或运行更顺畅。

请通过在GitHub仓库上发起问题来报告错误。这样我们能快速响应并直接处理问题。

## 翻译应用程序

我们欢迎帮助把应用程序翻译成地球上的任何语言。Zettlr使用`gettext`系统来翻译内容。

翻译与仓库中此应用的[程序源代码一起维护](https://github.com/Zettlr/Zettlr/tree/develop/static/lang)。进行翻译需要有一个GitHub帐号，但不需要技术知识。

!!! 注意

    如果你具备技术知识，也可以跳过下面的解释，直接[克隆仓库](https://github.com/Zettlr/Zettlr)。

要改进翻译，转到`static/lang`文件夹，下载与你要改进的语言代码相对应的`*.po`文件（例如，巴西葡萄牙语的`pt-BR.po`）。

下载文件后，你将需要一个程序来修改翻译。我们建议使用POedit。它还提供“专业”版，但你进行翻译不需要那个版本。

修改了你认为需要改进的翻译，接下来是将翻译添加到应用程序中。(如何在GitHub上提交更改)(https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files#editing-files-in-another-users-repository)是一个很棒的指南，请按照步骤进行操作。

### 创建新的翻译

如果你想创建一个翻译语言文件尚不存在的翻译，这个过程会更复杂一些。

!!! 注意

    如果你对自己在创建新翻译方面的能力没有信心，请与我们联系。我们将很高兴为你创建相应的文件，以便你随后依照上面的简单步骤。

1. 创建新的翻译文件，请确保计算机上已安装`gettext`系统
2. 克隆仓库：`git clone https://github.com/Zettlr/Zettlr.git`
3. 进入目录：`cd Zettlr`
4. 运行初始化命令（将`<lang>`替换为相应的语言代码，例如"pt-BR"或"de-DE"）：`msginit --input=static/i18n.pot --locale=<lang> --output=static/lang/<lang>.po`
5. 翻译目录中应该出现了一个名为`<lang>.po`的新文件，开始翻译，结束后发起PR。

## 开发

开始开发前，请[fork仓库](https://github.com/Zettlr/Zettlr)，接着就可以完成开发功能、错误修复等任务，然后发起pull请求。请记住**仅对develop分支发起PR！**master分支仅在新版本起草完毕接受推送。因此，如果你正在开发新功能同时Zettlr发布了新版本，你可以直接拉取
`upstream master`保持同步并继续手头的新功能开发。

准备开始做某项开发时，请不要忘了在issue追踪板块提出你正在做的事，这样我们能了解到有哪些工作正在进行。

!!! 注意

    这是[开发指南的README](https://github.com/Zettlr/Zettlr#contributing-code), 包括了安装说明、现有命令的文档。
