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

本项目适合快速建立简单的结构，如果你懂VuePress配置，并且需要的配置很多，那么可以在本项目生成简单结构的基础上，进行快速拓展。

- [VuePress官网](https://vuepress.vuejs.org/zh/)
- [作者个人笔记博客](https://zhukunpenglinyutong.github.io/)

> "我如果有空闲时间的话，就会思考怎么提高效率，节省时间" --- 朱昆鹏

## 🎖使用

```sh
# 安装
npm install vuepress-es --save

# 生成配置文件（建议三项全选）
npx vpe config

# 预览
npx vpe serve

# 打包
npx vpe build

# 生成一个初始化项目（未开放）
npx vpe init
```

---

## 🎗第一版功能说明

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