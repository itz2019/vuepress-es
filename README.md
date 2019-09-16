<p align="center">
  <img width="180" src="https://raw.githubusercontent.com/vuejs/vuepress/master/packages/docs/docs/.vuepress/public/hero.png" alt="logo">
</p>

<p align="center">
    <a href="https://www.npmjs.com/package/vuepress-es"><img src="https://img.shields.io/npm/v/vuepress-es" alt="npm版本号"></a>
    <a href="javascript:;"><img src="https://circleci.com/gh/itz2019/vuepress-es/tree/master.svg?style=svg" alt="CircleCI"></a>
    <a href="javascript:;"><img src="https://img.shields.io/npm/dw/vuepress-es" alt="每周下载量"></a>
    <a href="javascript:;"><img src="https://img.shields.io/github/license/itz2019/vuepress-es" alt="LICENSE"></a>
</p>

<h2 align="center">vuepress-es 可以让你快速使用vuepress，而不需要配置</h2>

VuePress是一个非常好的 静态网站生成器，我也使用这个构建了笔记文档，本着效率至上的原则，但是我感觉配置过程还可以再一步省略，提高生产效率。于是就有了本项目。

**本项目的定位如下：**

- 1.对于 VuePress没有配置成功过 的用户来说，提供一键化生成的效果（vpe init）
- 2.对于可以能进行基础配置，但是功能没有熟悉全的用户来说，提供快速生成配置，跟更快速的插件选择，第三方插件选择，让你的网站看起来更好一些
- 3.对于能配置 VuePress 95% 以上的用户，提供自行配置发挥的空间

- [VuePress官网](https://vuepress.vuejs.org/zh/)
- [作者个人笔记博客](https://zhukunpenglinyutong.github.io/)

> "我如果有空闲时间的话，就会思考怎么提高效率，节省时间" --- 朱昆鹏

## 🎖使用

```sh
# 安装
npm install vuepress-es --save

# 初始化（可以生成一个基础结构，并启动预览）
npx vpe init

# 预览
npx vpe serve

# 打包
npx vpe build

# 生成配置文件（没有配置文件的时候使用，用这个生成初始化配置文件）
npx vpe config
```

---

## 🌈示例演示

- npm init
- npm install vuepress-es --save 

**在根目录建立如下文件夹格式**

<img src="https://itzkp-1253302184.cos.ap-beijing.myqcloud.com/github%E5%9B%BE%E7%89%87/vuepress-es/%E7%A4%BA%E4%BE%8B%E6%BC%94%E7%A4%BA/1%E7%A4%BA%E4%BE%8B.png" />

- npx vpe config（会生成三个文件）
- npx vpe serve

<img src="https://itzkp-1253302184.cos.ap-beijing.myqcloud.com/github%E5%9B%BE%E7%89%87/vuepress-es/%E7%A4%BA%E4%BE%8B%E6%BC%94%E7%A4%BA/2%E7%A4%BA%E4%BE%8B.png" />

**文字在哪里设置，都备注好了，我解释一下 vpe.config.json 这个文件 的 folderShowOrder属性配置**

此属性可以完全自定义导航栏展示的顺序和名称 和 侧边栏展示的顺序，如果你没有特殊的展示顺序需要，只需要更改显示名称即可，我现在只把folderShowOrder改一下试试

```js
{
    // 左上角的标题（也是首页图像下面的一级标题）
    "title": "在vpe.config.json 中 配置 title",
    // 首页头像下面标题的解释
    "description": "在vpe.config.json 中 配置 description",
    // 右上角 跳转GitHub的地址（写一个GitHub项目地址）
    "repo": "https://github.com/itz2019/vuepress-es",

    // 设置侧边栏是否全部默认展开（一般官方介绍经常使用这个）
    "collapsable": true, // 注意：false 是展开，true 是不展开
    // 代码块是否显示行号
    "lineNumbers": false,

    // 文件夹展示顺序（有需求就进行设置，不仅可以设置需要显示的文件夹，还能设置展示的顺序，这里可能有点绕）
    "folderShowOrder": [
        {
            "title": "b",
            "alias": "我是文件夹b，默认上，我应该在后面",
            "childrenFolder": ["b-2", ]
        },
        {
            "title": "a",
            "alias": "我是文件夹b，默认上，我应该在前面",
            "childrenFolder": ["a-2", "a-1"] // ❣️ 这里的二级目录只是调换位置用的，不能修改名称
        },
    ]
}
```

**修改之后的效果**

<img src="https://itzkp-1253302184.cos.ap-beijing.myqcloud.com/github%E5%9B%BE%E7%89%87/vuepress-es/%E7%A4%BA%E4%BE%8B%E6%BC%94%E7%A4%BA/3%E7%A4%BA%E4%BE%8B.png" />

---

## ❣️注意事项

- 1.首层的文件夹一定要是 英文，否则会有问题（这个VuePress的问题，一时间没办法更改）
- 2.npx vpe serve 会启动一个预览，但是如果预览期间修改内容，不会实时更新
- 3.如果你新增，删除文件，那么vuepress-es会自动更新上，但是如果你修改文件夹结构，那么需要先在 vpe.config.js 中 修改可以显示的文件夹

---

## 🎗第一版功能说明

> v1.0.0 --- v1.3.2

### 1.基础功能实现

- [x] 建立文件夹，和.md文件，就能生成网站，用户不用管如何去配置的问题
- [x] 网址根目录 配置（建立 HOME.md）
- [x] 跳转目录首屏显示内容 配置（建立 RECORD.md）

---

### 2.优化第一版功能

- [x] 完善配置的功能，使其可以可视化的配置大部分的选项（建立 vpe.config.json）
  - [x] 基础配置
    - [x] 设置标题
    - [x] 设置标题的解释
    - [x] 设置右上角GitHub跳转链接
  - [x] 🔥 文件夹展示顺序（导航栏配置 & 侧边栏配置）
  - [x] 其他配置
    - [x] 侧边栏是否全部默认展开
    - [x] 代码块是否显示行号
  - [x] 增加 初始化展示 vpe init
  - [x] 可配置插件点击图片放大（可选）
  - [x] 增加不覆盖.vuepress/config.js的选项（并且默认更新导航栏和侧边栏）
