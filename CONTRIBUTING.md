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
