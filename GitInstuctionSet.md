# Git 指令集

| 序号 | 指令                                                     | 使用说明                                                     | 作用                                                       |
| ---- | -------------------------------------------------------- | ------------------------------------------------------------ | ---------------------------------------------------------- |
| 1    | git  config                                              | git config user.name  "your name"                            | 基本配置，配置用户名                                       |
| 2    |                                                          | git config user.email   "youremailname@example.com"          | 基本配置，配置用户邮箱                                     |
| 3    | git  init                                                | 需要要指定的目录下使用 `git init`  指令                      | 初始化git 仓库(在指定的目录下自动创建了一个 .git 的文件夹) |
| 4    | git  add                                                 | git  add  "filename."   可以多次使用本指令将多个文件提交到暂存区 | 将文件添加到暂存区                                         |
| 5    | git commit                                               | git commit -m "描述说明"   （最好配合使用 `-m "描述说明"`  来使用  git commit 指令） | 将暂存区的文件提交到仓库                                   |
| 6    | git status                                               | 随时都可以使用 `git status`  指令来查看git工作状态。它会根据实际给我们返回相应状态说明,如果工作区内容有修改，但未添国到暂存区，状态查询会反馈有修改，修改内容会以红色字体显示，当执行完 `git add` 指定，也就是修改内容添加到暂存区内后，再来查询状态，被修改的文件会以绿色字体显示，当执行完 `git commit`  指令后，再来查询状态，会告诉我们：分支中没有可提交的内容，工作树很干净 | 查询当前状态                                               |
| 7    | git diff                                                 | 仅当修改了内容但尚未添加到暂存区之前，使用 `git diff` 指令方可查询到修改的部分（也就是与已存版本不同的部分内容） | 顾名思义就是查看difference                                 |
| 8    | git log                                                  | git log 指令可以在终端中打印提交的历史记录.还可以使用 `git log --pretty=oneline`  以单行显示历史记录 | 查看历史记录                                               |
| 9    | git reflog                                               | `git reflog`   指令用以查看命令历史                          | 查看命令历史                                               |
| 10   | git reset                                                | `git reset --hard HEAD^`   回退到上一个版本   `git reset --hard HEAD^^`  回退到上上个版本   `git reset --hard HEAD~100`  回退到第100个版本    `git reset --hard 3a4d123(commit_id)`  回退到指定版本 | 回退版本                                                   |
| 11   | git checkout -- file                                     | `git checkout --file`  指令可以撤销修改,他只能撤销没有添加到git仓库(包括暂存区,和分支,也就是说修改完成后未曾使用过 `git add `  或  `git commit` 指令 )   **请注意,在使用 `git checkout`   指令时,如果是想要撤销修改,其后必需要跟  `--file`   否则,它将执行*切换到另一个分支* 的指令    该指令还可以对删除文件的操作进行恢复性操作** | 撤销修改(或撤销删除)                                       |
| 12   | git restore <file>                                       | 和上个指令一样，可以将工作区修改的内容删除掉，或者叫撤销修改。 其指令格式就是：`git restore <file>` | 撤销修改                                                   |
| 13   | git reset HEAD <file>                                    | `git reset HEAD <file>` 指令可以将添加到暂存区的修改内容撤回到工作区 **请注意：git reset 指令不仅可以做版本回退，还可以从暂存区将修改内空撤回到工作区** | 从暂存区撤回到工作区                                       |
| 14   | git restore --staged <file>                              | `git restore --staged <file>` 指令与上个指令功能一样，都 可以将添加到暂存区的修改内空撤回到工作区 | 从暂存区撤回到工作区                                       |
| 15   | git rm <file>                                            | `git rm <file>`  指令可以将添加到版本库分支中的文件进行删除.  **请注意:仅对添加到版本库分支中的文件可以使用该指令(*因为未添加到分支的中文件可以直接撤销\删除*),第二,执行完删除指令后,别忘了再向版本分支提交一次删除说明 .即 `git commit -m "说明文字"`** | 删除版本库中的文件                                         |
| 16   | ssh-keygen -t rsa -C "youremail@example.com"             | `ssh-keygen -t rsa -C "youremail@example.com"`  在命令行里执行该指令可以生成SSH密钥 | 生成SSH密钥                                                |
| 17   | git remote add origin git@server-name:path/repo-name.git | `git remote add origin git@github.com:username/reposetoryname.git` | 关联远程库                                                 |
| 18   | git push -u origin master                                | `git push -u origin master`                                  | 向远程库提交                                               |
|      |                                                          |                                                              |                                                            |

