<p align="center">
  <img width="180" src="https://raw.githubusercontent.com/vuejs/vuepress/master/packages/docs/docs/.vuepress/public/hero.png" alt="logo">
</p>

<p align="center">
    <a href="javascript:;"><img src="https://img.shields.io/github/license/itz2019/vuepress-es" alt="LICENSE"></a>
    <a href="https://www.npmjs.com/package/vuepress-es"><img src="https://img.shields.io/npm/v/vuepress-es" alt="npm版本号"></a>
    <a href="javascript:;"><img src="https://img.shields.io/github/repo-size/itz2019/vuepress-es" alt="repo-size"></a>
    <a href="javascript:;"><img src="https://img.shields.io/github/last-commit/itz2019/vuepress-es" alt="最后一次提交"></a>
</p>

<h2 align="center">vuepress-es 可以让你快速使用vuepress，而不需要配置</h2>

VuePress是一个非常好的 静态网站生成器，我也使用这个构建了笔记文档，本着效率至上的原则，但是我感觉配置过程还可以再一步省略，提高生产效率。于是就有了本项目。

本项目适合快速建立简单的结构，如果你懂VuePress配置，并且需要的配置很多，那么可以在本项目生成简单结构的基础上，进行拓展。

- [VuePress官网](https://vuepress.vuejs.org/zh/)
- [作者个人笔记博客](https://zhukunpenglinyutong.github.io/)

> "我如果有空闲时间的话，就会思考怎么提高效率，节省时间" --- 朱昆鹏

## 🎖使用

```sh
# 依赖（需要安装vuepress）
npm install vuepress --save

# 安装
npm install vuepress-es --save

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
- [ ] 首页 README.md 配置
- [ ] 三级目录结构的 README.md 配置

---

### 2.优化第一版功能

- [ ] 完善配置的功能，使其可以可视化的配置大部分的选项（建立 vpe.config.json）
  - [ ] 导航栏配置
  - [ ] 侧边栏配置
  - [ ] 搜索框配置
  - [ ] 其他配置