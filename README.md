git使用步骤
1、首先在本地创建ssh key
ssh-keygen -t rsa -C "your_email@youremail.com"
2、后面的your_email@youremail.com改为你在github上注册的邮箱，之后会要求确认路径和输入密码，我们这使用默认的一路回车就行。成功的话会在~/下生成.ssh文件夹，进去，打开id_rsa.pub，复制里面的key。
回到github上，进入 Account Settings（账户配置），左边选择SSH Keys，Add SSH Key,title随便填，粘贴在你电脑上生成的key。
3、为了验证是否成功，在git bash下输入：
ssh -T git@github.com
4、设置username和email，因为github每次commit都会记录他们。
git config --global user.name "your name"
git config --global user.email "your_email@youremail.com"
5、进入要上传的仓库，右键git bash，添加远程地址：
git remote add origin git@github.com:yourName/yourRepo.git
6、git init 以创建新的 git 仓库
7、git add <filename>
git add *
这是 git 基本工作流程的第一步；使用如下命令以实际提交改动：
git commit -m "代码提交信息"
8、提交到githubshang
git push origin master
成功后会看到Compressing objects: 100% (3/3), done.
