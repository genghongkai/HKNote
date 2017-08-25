## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/genghongkai/HKNote/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### the methods that pushing my product by git

```markdown
Syntax highlighted code block

1. Command line instructions(命令指令行)
Git global setup(先设置git全局设置)    #如果以前设置过则可以忽略
git config --global user.name "张三"   #设置git用户名
git config --global user.email "collinswang@21cn.com"    #设置git用户邮箱

# 方法一:(从零开始新建本地仓库,将远程文件clone下来)
Create a new repository     #本地新建仓库

git clone git@192.168.2.250:collins/front.git  #将远程git仓库文件clone至本地新建仓库
cd front                                    #切换至新建的分支
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master
# 方法二:
Existing folder     #已经存在文件夹(此目录之前未建立过远程git仓库连接)

cd existing_folder     #切到已存在的目录下
git init                      #初始化git
git remote add origin git@192.168.2.250:collins/front.git     #建立远成仓库连接
git add .                  #添加文件
git commit              #提交
git push -u origin master    #push到远程仓库

# 方法三:
Git repository    #已经存在的git仓库分支

cd existing_repository_folder     #切到已存在的git分支的目录下
rm -rf .git                          #删除该分支之前的git配置
git init                            #初始化git
git remote add origin git@192.168.2.250:collins/front.git     #建立新的远成仓库连接
git add .                  #添加文件
git commit              #提交
git push -u origin master    #push到远程仓库


**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/genghongkai/HKNote/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
