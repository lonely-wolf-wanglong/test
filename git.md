# github

## git与github

- git与github是完全不同的两个东西，在GIt中，开发者将源代码存入名为Git仓库的资料库中并加以利用。而github则是网络上提供git仓库的一项服务。

## Pull Request

- Pull Request是指开发者在本地对源代码进行更改后，向github中托管的git仓库请求合并功能。还可以对指定的一行代码进行评论。

## GitHub Flavored Markdown

- 在github上，用户所有用文字输入的功能都可以用github flavored markdown（GFM）语法,进行描述。

## Git

- 属于分散型版本管理系统，是为版本管理而设计的软件。

- Linux创始人Linus Torvalds在2005年开发了git的原型程序。

- 版本管理：就是管理更新的历史记录。
  - 集中型版本管理（Subversion）：将仓库集中存放在服务器之中，所以只存在一个仓库。集中型将所有数据集中保存在服务器中，有便于管理的优点。但是一旦开发者所处的环境不能连接服务器，就无法获取最新的源码，开发就无法进行。
  - 分散型（Git）：Github将仓库fork给了每一个用户，fork就是将github的某个特定仓库复制到自己的账户下。fork出的仓库与原仓库是两个不同的仓库，开发者可以随意编辑。
  
- Linux下gIt安装:sudo apt install git

- 设置使用git时的用户名和邮箱
  - git config --global user.name "lonely_wolf_wanglong"
  - git config --global user.email "2532306641@qq.com"
  - git config --global color.ui auto(可以让命令的输出拥有更高的可读性)
  
- 设置SSH
  - ssh-keygen -t rsa -C "2532306641@qq.com"生成 SSH key,需输入密码。其中id_rsa文件是私有密钥，id_rsa.pub是公开密钥。、
  - 输入ssh -T git@github.com可以与github进行认证和通信。
  
- 克隆仓库:git clone git@github.com:lonely-wolf-wanglong/test.git

- git基本提交代码到github的过程

  ```
  git add hello_world.php
  git commit -m "add a HelloWorld java file"
  git log //查看日志
  git status:查看状态
  git push:推送文件到github
  ```



### git基本操作

- git init 初始化仓库：会在目录下生成.git目录，.git目录里面存储着管理当前目录内容所需的仓库数据。

  ```
  mkdir git-tutortial
  cd git-tutortial
  git init
  ```

- git status:查看仓库的状态

- git add:向暂存区中添加文件，暂存区是提交之前的一个临时区域。

- git commit :可以将当前暂存区中的文件实际保存到仓库的历史记录中。通过这些记录，可以在工作树中复原文件。

- git log:查看提交日志。如果只想显示第一行简述信息，可以输入:git log --pretty=short。如果在git log命令后面加上目录名或者文件名则只会显示与该文件相关的日志。如果想查看提交所带来的改动，可以加上-p参数。

- git diff:可以查看工作树，暂存区，最新提交之间的差别。git diff HEAD:可以查看与最新提交有什么区别。

