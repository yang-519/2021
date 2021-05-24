# 2021
四段
本文档只针对练习使用





版本控制工具：
GIT  分布式版本控制系统
   1.版本控制系统
    开发中把每次的修改都有效的记录  （记录成一个版本），后期如果需要回退到原有的版本 或则只用当前和之前的版本进行比较，都可以有效的进行管理
   常用的版本控制系统 SVN  和 GIT
  
  SVN:集中式
客户端A                                                            客户端B
                                中央服务器
                                   
 代码A                       历史记录一 / 2             获取服务器最新的的代码   
 从服务器把代码拉取到本地，
集中式：所有的历史版本，都是在服务器上的，本地就是开发环境，本地开发完推到服务器服务器有历史版本拉取最新代码，也需要有服务器  必须连网

  GIT:分布式就是每个开发者都是一个仓库，都能记录历史版本信息不需要连网，
客户端A                   服务器                        客服端B
 A1                         同步                             B1

 A1                                                            B2
把中央服务器信息拉取下来

区别？
    1.git按照数据源传输  svn 按照问价传输    git比svn块
3.linux 团队开发git   

常用的linux命令
   ls  查看当前目录结构
  clear  清屏
   mkdir   创建文件夹名字
   cd  文件夹名：   进入文件夹
  touch    1.js   创建空文件
  cat     1.js   查看有啥
   vi 写内容   i
  ：wq    
红色：工作区
绿色:暂存区

git   add  .   提交
  git rm --cached  把暂存区的某个问件撤回到工作区
  git  rm  --cached .   -r   撤销暂存区中所有提交的


git  commit
git    pull
git puh   



git  创建仓库
  团队协助:每个人都有单独的本地仓库，有一个中央仓库

 客户端 A        客户端B
  版本A1            版本B1

  版本A2            版本B2





人数：
  一段：  10
  二段：23
 三段：山东14  北京28
 四段   ：45
 五段  ：21 
 六段 

css 写样式
  1. 行内样式
   <p style="css 语法"></p> 
 2.  内嵌样式
   1.在头部head 标签下写 style 标签
   <style>
       标签名{ css语法}
  </style>
 3. 链接样式
   1.新建一个css  文件    比如 1.css
   2. 在head 标签下 写   <link rel="stylesheet" href="css路径">
   3. 在css 文件直接写样式       标签名{ css语法}












常用版本控制系统
  svn（集中式）：
  git（分布式）：分布版本控制系统
开发中我们把每一次的修改都有效的进行记录（记录成一个版本）后期我们如果需要回退到原有的一个版本，或则是当前的某一个版本进行比较， 就可以有效的进行管理
svn和GIT的区别？
git的安装： 一路next即可
linux团队开发的git  git中的命令大部分都是linux 的命令

linux常用的操作命令
 提示： linux部分的命令和window doc的命令是类似的 但是不是相同的  git bash here 使用linux的
后期我们基本上都是基于命令来完成git管理的
 windows 操作系统：DOS窗口，DOS命令   
linux服务器操作系统： linux命令（MAC的终端使用linux的命令）
命令：
     ls -l / -a 查看当前目录结构的  （-a 查看的所有的包含隐藏）
     cd  xxx【路径地址】：进入到执行的文件夹中（路径可以粘贴到窗口中  右键pa）
      cd   /：根目录
      cd    ./ ：当前目录
      cd  ../  ：上级目录
  clear :清屏
 mkdir 文件夹的名称 ： 创建文件夹
 touch 文件的名称：  创建空的文件
  vi 文件的名称：向文件中写内容的
     i =》进入的插入模式
    esc +  ：wq  退出内容的插入模式  ，把刚才编辑的内容进行保存

 echo：向指定的文件中插入内容
cat 文件名称  查看文件中的内容
cp ：  拷贝
rm：删除文件 -r（递归删除） -f（强制删除）  一旦删除无法还原

GIT常规的流程
  每一个GIT仓库都有3个区
   工作区：写代码
   暂存区：临时存放每一次修改的代码，但是没有生成历史版本
   历史区： 存放所有的历史版本（提交到历史区就会生成一个历史版本）




添加到暂存区
git  add 文件名   ：  把工作区指定的文件名放在暂存区
git add .  包含修改和增加的一起放在暂存区

把暂存区的某一个文件撤回到工作区
git  rm  --cached 撤回文件名
git rm --cached  .  -r 把暂存区所有的都撤回到工作区
git rm --cached 1.txt -f  如果在撤销的过程中，发现从暂存区撤销的文件在工作区已经被修改了，只有加上  -f  才能强制从暂存区把内容删掉   
git  checkout  xxx.xxx  提交到暂存区一份，把工作内容改了，但是该的东西不好，想把暂存区上次提交的内容撤回到工作区（覆盖工作区新的内容）

添加到历史区
  git commit -m '备注的信息'


GIT  使用第一件事需要进行配置
 一.基础的配置的命令
   git config -l
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

git  init  ==》  git status  ==》  git add  名称 (暂存区) ==》 git commit -m“备注”历史区
  
二.真实项目中，并不是所有的文件都和项目有关系，也不是所有的文件都需要提交（node-modules 文件很大，这个文件肯定不需要提交）

.gitignore   ==》  git 提交忽略的文件
   生产环境
/node-modules 
  测试环境

git   log 查看历史版本信息

团队协作的流程
   每一个人都是单独的仓库， 有一个中央仓库，用来汇总所有开发则的编码信息的  （中央仓库一般是由项目经理创建的 ）
 1. 创建一个中央仓库： 可以基于 gitHub/codding来创建
http：//gitHub.com
  将开发者列入到仓库的开发群组中，每一个开发者都有自己的github账号，，都有权限可以操作这个仓库了

  2. 创建客户端本地仓库（一个开发者就是一个单独的仓库），还需要让本地的仓库和远程的仓库保持关联  ，这样才可以实现信息的同步

git init
连接远程仓库    
git remote add origin  远程厂库地址  https://github.com/yuanyuanJN/2021.git
git remote -v  查看连接信息  （origin连接名称)
移除远程连接仓库
git  remote rm  origin
更新远程连接仓库
git remote update  origin  
有一个更简单的方式，  只要把远程仓库克隆到本地

  git  clone 远程仓库地址
  git add .  添加到暂存区
  git commit  -m""  历史区
git pull origin master    本地代码和中央仓库代码保持一致
git push origin master  (每一次push之前需要先pull一下)  提交到中央仓库


中央仓库地址 https://github.com/yuanyuanJN/2021.git



yuanyuanJN


node==> 前提上必须安装node（注意一定要安装最新的node版本）
  node  -v 检测node的版本
  npm install  安装的名称  安装东西









    
