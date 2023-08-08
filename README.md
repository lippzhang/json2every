# json2every
一行json，生成一个页面或者系统

## RFC
[rfc-001](./rfcs/rfc-001.md)
## Quick Start

```bash
# Install Dependencies.
$ pnpm i 
# Build and link packages.
$ pnpm packages:build
# Start watch service
$ pnpm start
```

# 背景
开发中后台的页面的时候，经常遇到CRUD很相似的页面，大部分人都会将这些页面进行抽象。抽象的过程中，遇到了以下的问题：
* 有些很Magic的代码，让新手难以理解。
* JSON配置没有文档和examples，所有新人还需要看一遍源码，耗时耗力。
* 性能卡顿，一个组件，写了上千行的逻辑代码，执行逻辑缓慢，耗时。
* 老板某天看到觉得的UI交互不好看，过几天又觉得好看了，频繁的修改css逻辑。
## 最终目标
* 写页面只需要写 JSON，不管项目是 Vue2、Vue3 甚至是 React，不管组件库是 AntD、Element，Naive UI，写出来的 JSON 都一样。
* json -> transform(React/Vue/Angular, AntD/Element/Naive UI) -> page
* 使用rust语言保证性能。使用微内核架构，方便扩展，提高安全性，降低耦合性。

# TODO
- [x] 简单架构设计 rfc-001
- [x] 项目框架搭建和技术选型确定
- [ ] 接入github action： 
https://modernjs.dev/guides/topic-detail/changesets/add.html 
https://juejin.cn/post/7181409989670961207#heading-9
- [ ] 接入N-api，使用rust进行开发
- [ ] 项目核心开发
- [ ] 官方loader和plugin
- [ ] 项目测试和完善
- [ ] 项目推广

# 参考
* https://github.com/baidu/amis
* https://github.com/alibaba/lowcode-engine