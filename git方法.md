码云配钥

ssh-keygen -t rsa -C "*********@qq.com"

加入到网页仓库SSH key 中才可生成新的公钥

cat ~/.ssh/id_rsa.pub

码云下载

git clone "git*****************"（ssh链接，默认为桌面，可通过cd设置）

码云上传

​	1.先使用cd跳转目标路径git（$ cd "edge_technology"/test/"online_backup"/test（右斜杠））（与 .git 同路径）

​	2.git status（查看增加的文件，与.git 同路径）

​	3.git add .(增加至缓冲区git )(注意.前有空格)

​	4.git commit -m '（修改描述）'

​	5.git push（上传代码）

tip:没有仓库需新建仓库（git init）



错误：

Commit failed - exit code 128 received, with output: '*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: empty ident name (for <>) not allowed'

需要到项目 .git\config文件最后加入



[user]（自定）
    name = yannan
    email = 781369549@qq.com





加错路径false

无修改false