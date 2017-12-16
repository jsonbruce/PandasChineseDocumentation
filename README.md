# pandas 中文文档

> pandas 是一个非常强大的 Python 数据分析工具集

pandas 中文文档基于 pandas 官方文档(PDF Version)
 [pandas 0.21.0 documentation PDF  Version](https://pandas.pydata.org/pandas-docs/stable/pandas.pdf)

PDF Version 包含了章节序号，更方便索引。


# 在线阅读
使用 GitBook 制作，可以直接[在线阅读](https://jsonbruce.gitbooks.io/pandas-chinese-documentation)。


# 简介
`pandas 0.21.0` 发布于 2017.10.27，这一版本包含了许多重大的更新。

pandas 中文文档的目录结构依然保持 pandas 官方文档(PDF Version)的目录结构，但不同的是，目前不是完全翻译，是就重点章节进行部分翻译。

一个小的动机就是, *《利用 Python 进行数据分析》* 是一本非常优秀的数据分析书籍，但其内容基于 *python 2.7* 和 *pandas 0.9*，许多 API 现在已经发生了变化。


# 如何贡献
**GitHub Repository:** [PandasChineseDocumentation](https://github.com/jsonbruce/PandasChineseDocumentation)

## 认领翻译任务
在仓库的 `Issues` 下可以看到根据标签（Label）分类的翻译任务状态:

- `待翻译` : 表示还没有人认领这个翻译任务
- `翻译中` : 表明已经有人翻译了
- `待校对` : 表明此章节已翻译完成，正在等待校对
- `校对中` : 表明正在校对
- `校对完` : 表明校对完成，等待发布


## Cooperative Translate Flow (CTF)

1. Fork 我仓库 [PandasChineseDocumentation](https://github.com/jsonbruce/PandasChineseDocumentation)
2. Clone 到你本地
3. 运行 `git checkout -b develop` 创建并切换到 develop 分支
4. 运行 `git remote add upstream https://github.com/jsonbruce/PandasChineseDocumentation` 将我仓库添加为远端库
5. 运行 `git remote update` 更新
6. 运行 `git fetch upstream master` 拉取我仓库的更新到你本地
7. 运行 `git rebase upstream/master` 将我仓库的的更新合并到你 develop 分支

这是一个初始化流程，只需要做一遍就行，之后请一直在 develop 分支进行修改。

8. 运行 `git add .` 添加更新
9. 运行 `git commit -m [message]` 提交到本地仓库
10. 运行 `git push` 推送更新到 GitHub
11. 在 GitHub 发起 `Pull Request`


# 贡献列表
- [jsonbruce](https://github.com/jsonbruce)


# 开源协议
[GNU GPL v3.0](https://choosealicense.com/licenses/gpl-3.0)
