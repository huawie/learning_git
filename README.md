# learning_git  
学习git技术  

>1 配置一下ssh key 提供对服务器内容的读写权限:   
>>1-1 git bash here (C:\Users\harveyhwliu)  
>>1-2 生产SSH公钥 ssh-keygen -t rsa -C "github上的邮箱",公钥在C:\Users\harveyhwliu\.ssh 目录下有一个**_rsa.pub的文件  
>>1-3 把这个公钥id_rsa.pub的内容复制一下,配置到github ->setting -> ssh and gpgkeys-new ssh key上  


>>2 常用命令  

 | Git 命令    |    解释 |  
 | :-----  | :--------|  
 | git init    | 本地仓库（repository）初始化 |  
 | git remote add origin https://github.com/harveyhwliu/learning_git.git   |添加远程库 | 
 | git push -u origin master    | 将本地master分支代码推送远程代码库origin  本地仓库不能为空，否则报错。| 
 | git add add.php     | 把工作区文件提交到暂存区 | 
 | git commit -m "comments"     | 把(git add 的结果)暂存区文件统一提交到本地仓库| 
 | git pull --rebase origin master     | 为了避免git push 时产生菱形，保持提交曲线为直线| 
 | git config --global core.editor "'D:/InstallSoftWare/Sublime Text 3/sublime_text.exe' -n -w"     | 配置git commit 默认编辑器| 
 | git config --global push.default upstream     | default 默认是nothing，需要 git push origin branchname，指定upstream : push当前分支到它的upstream分支上|  
 | git config --global merge.conflictstyle diff3     |改进冲突标记使其也显示（分支）共同祖先 | 
 | git config --global user.name "Your Name"     | 设置用户名| 
 | git config --global user.email you@example.com     | 设置用户邮箱 | 
 | git config --system core.longpaths true     | 解决clone时超出了 Windows 的路径长度限制的错误|  
 | git reset \[文件\]     | 将add的文件从暂存区删除，工作目录仍然存在| 
 | git branch     | 查看所有分支|  
 | git branch fix_bug_1     |创建分支 |  
 | git checkout -b fix_bug_2      | 创建并检出分支fix_bug_2| 
 | git checkout fix_bug_1     | 切换分支| 
 | Git log     | Git log是以指定的commit或者指定分支的的最新commit为起点，向前跟踪，直至commit没有父commit,因此存在不可达的commit| 
 | git merge branch2 branch3     |-	如果检出了 branch1 ，则合并的版本会将 branch1 以及 branch2 和 branch3 组合起来| 
 | git merge --abort     |将文件恢复到你开始合并之前的状态 | 
 | git config --global core.autocrlf true     |解决CRLF LF 所导致的合并冲突问题 | 
 |  git show commit_id    |5.	分支比对命令 将提交与所在分支进行对比 | 
 |  git fetch origin    | 更新远程跟踪分支| 
 | git pull origin master     | 将远程代码库origin内容拉取到本地master分支| 
 |  git push origin master    | 将本地master分支代码推送远程代码库origin| 
 |  git remote -v     |查看远程代码库详细信息 | 


（git 初始化）
git clone （拷贝远程仓库）
git add （git 添加）
git reset [文件]  (将add的文件从暂存区删除，工作目录仍然存在)
git commit -m "Commit message"  （提交git add的结果到repository）
git commit -a -m "Commit message"  (提交repository）

git log -n  1
git status （git 状态）
staging area （暂存区）--- git add 的结果
working directory （工作目录）
repository	（仓库） --- git commit 的结果
git diff ID1 ID2
git checkout ID2
git log --graph --oneline master 分支名  直观地查看提交历史记录
