## 技术栈

nodejs + koa2 + es6/7 + redis + nginx + mysql +md5 + pm2+ koa-logger + koa-onerror

## 项目运行

```
项目运行之前，请确保系统已经安装以下应用
1、node (10.12.4 及以上版本)
2. 导入表 手动写入code2Session表appid，appSecret
```

```

cd blogs-wechat-koa

npm install

npm run serve

pm2 deploy deploy.yaml production upddate

```

小程序目录,直接导入就可以了

```
blogs-wechat-koa/views/WXpodcast
```


## 目标功能

- [x] 文章详情 -- 完成
- [x] 文章分类 -- 完成
- [x] 文章列表 -- 完成
- [x] 获取用户信息 -- 完成
- [x] 用户收藏 -- 完成 ✨✨
- [x] 个人中心 -- 完成
- [x] 测试接口 -- 完成
- [x] 用户点赞 -- 完成
- [x] 用户授权绑定-- 完成
- [x] 我的收藏列表 -- 完成
- [x] 每日签到 -- 完成
- [x] 用户信息解密 -- 完成
- [x] 工具类 -- 完成
- [x] 服务配置 -- 完成
- [x] 面具接口 -- 完成
- [x] 获取文章评论 -- 完成
- [x] 插入文章评论 -- 完成
- [x] 管理员权限验证 --
- [x] 超级管理员 --
- [x] 日志输出 -- 完成
- [x] 详情错误 -- 完成
- [x] 前后台路由同构 -- 完成


## 项目布局

```
.
├── blogs-wechat     koa2后端服务项目(前后端分离)
│   │
│   ├── api
│   │   └── index.js                  koa2-mysql数据池连接封装
│   ├── config
|   |     └── index.js                服务与数据库配置
│   ├── controller
│   │   ├── admin                     后台管理系统控制器
│   │   └── web                       前台系统控制器
│   │       ├── articleDetail.js      文章详情接口
│   │       ├── articleType.js        文章分类接口
│   │       ├── articleTypeList.js    文章列表接口
│   │       ├── authorization.js      获取用户信息接口(解密用户信息ok)
│   │       ├── collect.js            收藏接口
│   │       ├── getUserSignList.js    个人中心接口
│   │       ├── index.js              测试接口
│   │       ├── like.js               点赞接口
│   │       ├── login.js              用户授权绑定接口
│   │       ├── myCollectList.js      我的收藏列表接口
│   │       ├── insertComment.js      插入文章评论
│   │       ├── getComment.js         获取文章评论接口
│   │       ├── maskVersion.js        面具接口
│   │       └── sign.js               签到接口
│   ├── db
│   │   └── index.js                  数据连接
│   ├── node_modules
│   │   └──xxx.js                     依赖包
│   ├── redis
│   │   └── index.js                 redis配置封装
│   ├── routes
│   │   └── index.js                 后端路由
│   ├── utils                        工具类
│   │   ├── examineToken.js          token过期配置封装
│   │   ├── isObject.js              判断对象是否为空
│   │   ├── time.js                  时间处理
│   │   └── WXBizDataCrypt.js        wechat用户解密算法
│   ├── views                        前端静态文件托管
│   ├── .gitignore                   git忽略文件
│   ├── deploy.yaml                  pm2自动发布配置
│   ├── index.js                     服务配置
│   ├── package-lock.json            包的版本号(快速下载依赖链接)
│   ├── package.json                 模块(npm run server/依赖包)
│   │
│   └──README.md                     文档说明
.


```

