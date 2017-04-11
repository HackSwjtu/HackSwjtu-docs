# HackSwjtu - Git 使用规范

## 事项注意

+ 多人协助时使用 `git pull`，避免使用 `--rebase` 参数进行代码覆盖操作。
+ 使用 *Git* 过程中，最好创建分支进行开发。*Coding Reviewer* 的人员有责任检查其他同事是否遵循分支规范；
+ 在 *Git* 中，默认是不会提交空目录的，如果想提交某个空目录到版本库中，需要在该目录下新建一个 `.gitignore` 的空白文件，即可以提交。
+ 把外部文件纳入到自己的 *Git* 分支来的时候一定要记得是先比对，确认所有修改都是自己修改的，然后再纳入。
+ 每个人提交代码是一定要 `git diff` 看提交的东西是不是都是自己修改的。否则很有可能是版本冲突代码。

## 提交 Message 规范

### 格式

```git
[修改类型]:[提交信息] [issue 参数(optional)] [githook 参数(optional)]
```

修改类型包括：

+ MOD：代码修改
+ ADD：文件增添
+ FIX：Bug 修正
+ MEG：merge 操作
+ SOL：冲突解除操作
+ DOC：`README 文档`编辑

## Git 配置

```git
$ git config --global user.name "[用户名]"
$ git config --global user.email "[邮箱]"
$ git config --global merge.tool "[Merge 工具]"
$ git config --global --list # 查看配置信息
```

## githook 标准

HackSwjtu githook 配置、安装及使用方法请参看 [HackSwjtu/githook](https://github.com/HackSwjtu/githook) 文档。

## Git 相关教程推荐

[Pro Git](https://git-scm.com/blog/2010/06/09/pro-git-zh.html)

[廖雪峰 Git 教程](http://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)