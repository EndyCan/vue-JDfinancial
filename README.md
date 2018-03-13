# vue-JDfinancial

> vue2.0+sass+webpack

## 介绍

### 项目特点

* 模块化
* 自适应
* CSS Module

### 模块化

不仅对 js 模块化，也采用 sass/scss 实现 css 的模块化。

### 自适应

移动端自适应使用了[hotcss.js](https://github.com/imochen/hotcss)和[px2rem-loader](https://github.com/Jinjiang/px2rem-loader)。  
hotcss 使用动态的 HTML 根字体大小和动态的 viewport scale。在 vue 中配置 px2rem-loader，在开发时只使用 px，px2rem 把 px 转成 rem，再动态的计算 font-size。

### CSS Module

使用 css Module 防止命名冲突，它的工作原理是把一个类名编译成哈希字符串，然后在引用的时候直接使用这个哈希字符串字符串，进而保证相同的类名根据不同的路径和组件名称得到不同的值，保证了最终的类名隔离。  
[vue 中配置 CSS Module](https://vue-loader.vuejs.org/zh-cn/features/css-modules.html)

## App 目录结构

```
|-css/
|   |-element.scss   //css模块
|   |-reset.scss     //css样式初始化
|
|-js/
|   |-core/          //常用组件
|   |-download/      //App下载页
|   |-home/          //首页
|   |-ious/          //白条
|   |-mine/          //我的（未开发）
|   |-money/         //理财
|   |-public/        //公共组件
|   |-raise/         //众筹
|   |-router/        //路由
|   |-App.vue
|   |-main.js
|   |-viewport.js    //hotcss文件
|
|-view/
|   |-index.html     //html模板
```

### 安装运行

```
npm install
npm run start
```
