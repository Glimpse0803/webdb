## 介绍
这是一个基于Vue3+yii2的以人工智能为主题的视频文章展示与评论网站，实现了基本的视频文章展示功能，以及大模型对话功能。

## 部署
1. 安装Docker和Docker Compose
2. 克隆项目到本地
3. 进入项目目录，在根目录运行`docker-compose up -d --build`启动项目，请注意，这一步需要你拥有较好的网络环境
4. 在根目录执行`docker-compose  exec backend composer install  `下载PHP依赖
## 使用大模型对话功能
为了使用大模型对话功能，你需要在[月之暗面](https://www.moonshot.cn/)申请一个APIKey，并在项目前端目录创建一个`.env`文件，文件内容如下：
```shell
# .env
VUE_APP_MOONSHOT_API_KEY=你的moonshot api key
```
然后执行`docker-compose restart frontend  `重启前端即可



## 继续开发
如果你想继续开发这个项目，你可以在根目录运行`docker-compose -f docker-compose.dev.yml up -d --build`启动项目，然后在根目录执行`docker-compose  exec backend composer install  `下载PHP依赖，然后你就可以进行你自己的开发啦~