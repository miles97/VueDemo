## 项目中使用git工具

首先自然是安装git工具，确保右键菜单有git bash here 和 git GUI

图形界面更方便使用git工具来进行clone以及create

然后在git bash界面使用ssh-keygen -t rsa -C "YOUR NAME HERE" 创建本地的ssh 公用key

然后在gitlab工作台上复制上相应的ssh

然后进入项目 在主分支上创建自己的项目分支，通过小乌龟工具完成版本的控制管理功能，然后pull东西

### sourcetree

注册账号

通过视图化的界面进行拉取 推送 合并 

实际的操作还是比较简单的 没有什么可以多介绍滴

1.关于sourcetree的使用问题

cao-dev-branch  以及主分支 dev的问题

为什么需要在自己分支上开发的原因显而易见，按照我的理解就是不会污染主分支的时间线，在数次提交之后合并到主分支上，不造成时间轴污染


### webStorm PRODUCTION

1. 使用ctrl + ·  ,切换选择主题以及颜色以及基本功能使用（继承其他使用习惯IDE）

2. 格式化代码ctrl + Atl + L 



### IDE原则

1.由于部分IDE使用中的代码格式化可能会导致不同代码格式化的排版问题带来困扰

2.微信小程序原生开发工具效率太低 后续避免开发

3.项目文档方面的积累  

#### 常见的git操作手册

使用git config http.postBuffer 524288000进行第一次项目push的时候，防止默认缓存引起的提交问题

使用获取代替拉取  新建分支拉取后推送

