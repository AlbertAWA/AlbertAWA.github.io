## 个性化定制
### 基本配置
修改**config.json**：
```js
{
    "name": "your github username",
    "repo": "your github reponame",
    "client_id": "your client_id here",
    "client_secret": "your client_secret here",
    "title": "add your title",
    "instruction": "add your instruction",
    "server_link": "http://119.23.8.25/gh-oauth-server.php",
    "filter": {
        "creator": "all",	//@param: "all" or a username(eg. "imuncle")
        "state": "open"		//@param: "open", "close", "all"
    },
    "menu": {
        //add your menu items and URL here
        //example:
        //"Home" : "./",
        //"RSS" : "https://rsshub.app/github/issue/imuncle/imuncle.github.io",
        //"About me" : "content.html?id=41"
    },
    "friends": {
        //add your friends link here
        //example:
        //imuncle : "https://imuncle.github.io"
    },
    "icons": {
        //add your footer icons here
        //you can set a jump link or display an image
        //template :
        //"the title of the icon" : {
        //  "icon_src" : "the image of the icon",
        //  "href" : "the link you want to jump",
        //  "hidden_img" : "the image you want to show",
        //  "width" : the width of the hidden_img, this should be a number.(unit : px)
        //}
        //example :
        //"Github" : {
        //    "icon_src" : "images/github.svg",
        //    "href" : "https://github.com/imuncle",
        //    "hidden_img" : null,
        //    'width" : 0
        //}
    }
}
```
将自己的个人信息填写进去。

选项|含义
:--:|:--:
name|填写你的GitHub用户名
repo|填写你的pages对应的仓库，一般是：用户名.github.io
client_id|填写你申请OAuth APP时拿到的client_id
client_secret|填写你申请OAuth APP时拿到的client_secret
title|填写你的个人网站的标题
instruction|填写你的个人网站的简介
server_link|填写你的服务端地址，~~若没有服务器可填写`http://119.23.8.25/gh-oauth-server.php`~~ 该服务器已停用
filter|填写issue筛选规则，可根据creator和issue state筛选
menu|填写右侧菜单中的名称和链接
friends|填写你的网站的友链，若没有则不填写
icons|填写网站页脚的图标信息，若没有则不填写

上面的server_link是服务端的地址

如果你有服务器，那么你可以使用该PHP代码自己配置服务端，将**server_link**写为自己的服务端地址。

### 动态打字配置
网站首页有一个动态打字的效果，配置地方在**index.html**中。

找到如下代码（在尾部）：
```javascript
$("#changerificwordspanid").typed({
    strings: ["good", "happy", "healthy", "tall"],
    typeSpeed: 100,
    startDelay: 10,
    showCursor: true,
    shuffle: true,
    loop:true
});
```
可以更改`strings`来更改单词。

### 图片更改
图片全部都存储在**images**文件夹中。

图片名称|含义
:--:|:--:
404.png|404页面
avatar.jpg|网站图标
fish.png|404页面
github.svg|GitHub图标
house1.png|404页面
house2.png|404页面
page_backfround.jpg|首页的背景图
search.svg|右上角搜索图标
totop.png|右下角“回到顶部”按钮图标

如果没有前端知识，建议更改图片时不要更改文件名。
