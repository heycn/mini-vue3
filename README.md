<h1 align="center">mini-vue3</h1>

<p align="center">从零实现 Redux 过程 ( 深入深入学习 vue3 )</p>

## 为什么做这件事

最近，我的项目中使用到 `vue3`，但工作中更多使用的是 `react`，本着 `将技术吃透` 的理念，也看了 `vue` 相关的书籍，例如 `《Vue.js 设计与实现》`，但是最后发现一个问题：整个过程都是在「被动学习」，并没有没有「主动输出」，这种学习效果是比较差的，知识容易遗忘。

而我比较推崇 `费曼学习法` 的学习方式 —— 把复杂的知识简单化，以教代学，让输出倒逼输入。

一次偶然的机会，我在 `bilibili` 遇到了 [阿崔cxr](https://space.bilibili.com/175301983/?spm_id_from=333.999.0.0)，了解了他的 `mini-vue` 课程后，我对 `崔老师` 的一句话大为触动：`「掌握源码最有效的学习方法就是手写一遍！」`，我觉得这句话说的太对了，于是我便购买了他的课程，并且沉淀了每一集的内容，经过独立思考后输出了一个自己的 [mini-vue3](https://github.com/heycn/mini-vue3)，并且将实现过程的 `心得` 总结成了一篇篇博客

这样的学习过程就有了大量的「自我思考」，学习效果会相对好很多，而且我将其过程总结成了 `博客`，当不可避免地出现 `遗忘` 时，我回去看看我的博客，便能想起我当初的「心路历程」，这个学习方法我是从 [方应杭](https://www.zhihu.com/people/zhihusucks) 那里学到的 —— `「内存是有限的，当内存不够用的时候，我们就要借助外存」`。

## 我将如何做这件事

基于 vue3 的功能点，一点一点的拆分出来。

代码命名会保持和源码中的一致，方便通过命名去源码中查找逻辑。

TDD 测试驱动开发、小步走、重构手法、TPP...

### TODO

#### runtime-core

- [ ] 支持组件类型
- [ ] 支持 element 类型
- [ ] 初始化 props
- [ ] setup 可获取 props 和 context
- [ ] 支持 component emit
- [ ] 支持 proxy
- [ ] 可以在 render 函数中获取 setup 返回的对象
- [ ] nextTick 的实现
- [ ] 支持 getCurrentInstance
- [ ] 支持 provide/inject
- [ ] 支持最基础的 slots
- [ ] 支持 Text 类型节点
- [ ] 支持 $el api
- [ ] 支持 watchEffect
#### reactivity

目标是用自己的 reactivity 支持现有的 demo 运行

- [ ] reactive 的实现
- [ ] ref 的实现
- [ ] readonly 的实现
- [ ] computed 的实现
- [ ] track 依赖收集
- [ ] trigger 触发依赖
- [ ] 支持 isReactive
- [ ] 支持嵌套 reactive
- [ ] 支持 toRaw
- [ ] 支持 effect.scheduler
- [ ] 支持 effect.stop
- [ ] 支持 isReadonly
- [ ] 支持 isProxy
- [ ] 支持 shallowReadonly
- [ ] 支持 proxyRefs

### compiler-core
- [ ] 解析插值
- [ ] 解析 element
- [ ] 解析 text

### runtime-dom
- [ ] 支持 custom renderer 

### runtime-test
- [ ] 支持测试 runtime-core 的逻辑

### infrastructure
- [ ] support monorepo with pnpm
### build

```bash
pnpm build
```

## 如何使用

### example

通过 server 的方式打开 packages/vue/example/\* 下的 index.html 即可

>  推荐使用 [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
