# git使用

**一. 流程**

1. 进入文件夹，点击右键的 git bash ，弹出窗口输入命令git init进行初始化。生成 .git文件夹

2. 输入命令git status ，检测当前文件夹下文件的状态
3. 输入git add 文件名 表示管理该文件 （管理的文件显示绿色，未管理的文件夹显示红色）若输入 git add . 则表示管理所有文件；反之，用git reset 文件名 或 git reset .撤销该操作
4. 输入git commit -m '描述信息' 生成版本
5. 查看版本记录：输入git log；（新回到旧版本可以用git log 查看版本号，旧回到新版本可以用git reflog 查看版本号）
6. 若修改文件输入 git status 文件显示红色
7. touch 文件名 增加一个文件
8. 修改git commit 注释信息：

（1）git commit --amend

（2）按键i进入编辑

（3）按键Esc退出编辑

（4）输入:wq保存信息

9. 分支（主干名字为master）
   创建一个分支（从最新版本开始）git branch 分支名
   切换主干或分支 git checkout master/分支名

   分支合并到主干 git merge 分支名 （需要先切换到主干）
   删除分支 git branch -d 分支名
   合并分支时出现冲突可以手动修改提交
   工作流：master用稳定版的，而分支（dev）做开发
   cat 文件名 查看文件内容

