## 说明
GitHub改版之后的提交方式改为了令牌提交，需要测试一下

好像之前说过这个所谓的令牌提交就是在提交的时候账号不变，密码修改为这个【令牌】

也就是由【账号+密码】改为了【账号+令牌】的方式

<hr />

但是好像一次就成功了，通过在命令行初始化这个仓库，然后直接`git push`，之后git会弹出对话框，和之前不同的是，这个对话框有两个可选的框，左边的一个貌似可以通过浏览器登录GitHub，我使用的是右边的框，让输入token。

在将token输入之后，敲击回车就提交成功了，没有要求输入账号，可能是使用了全局账号？

在查看了控制台的Windows凭据管理器之后，确定了这个猜测，里面增加了两个今天创建的普通凭据，其中地址关联到GitHub上的那个凭据所使用的用户名就是xjy-1999

<hr />

上述操作仅限于对空仓库进行操作，如果是一个已经有内容的仓库（比如开源许可证或者自述文件）则可能会出现诸如文件冲突、重名文件、分支名不统一之类的问题。

最推荐的，要么远端建好，本地先拉取再提交；

要么远端建一个完全空白的仓库，所有内容由本地进行提交。