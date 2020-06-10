# 说明

## 背景

现在有一个资源网页（http://106.12.192.227:3000/），里面包含一些资源号（mxxxxxxxx），资源号随时会新增一些（新增的位置不定，但旧资源不会删除）。请编写一个爬虫，每次执行时检查这个页面，当有资源新增时，能够发现。


## 目标

> 完成此目标获得1颗星

每次运行完，如果有新增资源号，请将其写入data/output.data，如：

```
m91781946464
m91781946462
```

## 提示

现在src下有一个初始项目，做了少量工作

* npm install
* src目录下已经有初始代码了，通过npm run start 或 node_modules/.bin/ts-node src/index.ts均可执行，目前执行的结果是显示http://106.12.192.227:3000/的内容
* fetch-data.ts 已经写好了请求网页逻辑
* 你可以从init.ts 开始你的编写
* 每次抓取执行完毕，你可能需要存储当前已有的资源号，请放在data/existence.data
* 文件操作参考(writeFileSync, readFileSync)(https://www.runoob.com/nodejs/nodejs-fs.html)
* 如果你需要测试，可以自己设置proxy或使用本地api（http://localhost:3000/list），并修改server/example.data改变数据

```bash
cd server
npm install
npm start
```

## 进阶目标

> 完成此处目标可以获得更多星

* 实现日志功能，当异常时记录警告和错误(日志存放在log/下)
* 能够同时支持更多类型的接口
  * http://106.12.192.227:3000/json
  * http://106.12.192.227:3000/list

## 提交代码

完成工作请将代码提交到分支~

```
git push origin HEAD:yourname
```
