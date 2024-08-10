![CF-Gh-proxy-Github](https://socialify.git.ci/codebhc/CF-Gh-proxy-Github/image?description=1&language=1&logo=https%3A%2F%2Fimgos.cn%2F2024%2F08%2F09%2F66b61bcb2232b.jpg&name=1&owner=1&pattern=Circuit%20Board&stargazers=1&theme=Dark)

# CF-Gh-proxy-Github：Github代码仓库加速下载，青龙加速拉库工具

这个项目是一个基于Cloudflare Workers搭建gh-proxy。它能够加速下载仓库文件，解决青龙面板拉gitHub脚本库因网络问题导致慢或者拉取失败的问题。

## 部署
- **Workers** 部署：复制 [_worker.js](https://github.com/codebhc/CF-Gh-proxy-Github/blob/main/_worker.js) 代码，替换自动生成的代码，`保存并部署`即可
- **Python** 部署：太麻烦，如需要请查看原作者仓库：[**原作者项目地址**](https://github.com/hunshcn/gh-proxy)

## 绑定域名
转到Workers和Pages-概述-刚刚部署的worker-触发器，点击添加自定义域名，输入自己的域名（要完整，比如github.example.com），点击添加自定义域名。此时浏览器输入自己域名即可访问。


## 使用
### 路径前面加域名
下载文件，在链接前面加上自己的域名或者访问自己的域名(绑定了的)根据提示输入并下载

### 青龙面板拉取仓库加速
青龙面板里订阅，链接加上自己的域名就能加速拉取GitHub仓库。
如：原订阅填写
```
https://github.com/hunshcn/gh-proxy.git
```
很慢，换成
```
自己的域名/https://github.com/hunshcn/gh-proxy.git
```
