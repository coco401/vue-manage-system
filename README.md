# vue-manage-system

<a href="https://github.com/vuejs/vue">
    <img src="https://img.shields.io/badge/vue-3.2.8-brightgreen.svg" alt="vue">
  </a>
  <a href="https://github.com/element-plus/element-plus">
    <img src="https://img.shields.io/badge/element-plus@1.0.2-beta.52-brightgreen.svg" alt="element-plus">
  </a>
  <a href="https://github.com/lin-xin/vue-manage-system/blob/master/LICENSE">
    <img src="https://img.shields.io/github/license/mashape/apistatus.svg" alt="license">
  </a>
  <a href="https://github.com/lin-xin/vue-manage-system/releases">
    <img src="https://img.shields.io/github/release/lin-xin/vue-manage-system.svg" alt="GitHub release">
  </a>

基于 Vue3 + Element Plus 的后台管理系统解决方案。
[线上地址](https://lin-xin.gitee.io/example/work/)


## 项目截图

### 登录

![Image text](https://github.com/lin-xin/manage-system/raw/master/screenshots/wms3.png)

### 首页

![Image text](https://github.com/lin-xin/manage-system/raw/master/screenshots/wms1.png)


## 前言

该方案作为一套多功能的后台框架模板，适用于绝大部分的后台管理系统（Web Management System）开发。基于 Vue3，使用 vue-cli3 脚手架，引用 Element Plus 组件库，方便开发快速简洁好看的组件。分离颜色样式，支持手动切换主题色，而且很方便使用自定义主题色。

## 功能

-   [x] Element Plus
-   [x] 登录/注销
-   [x] Dashboard
-   [x] 表格
-   [x] Tab 选项卡
-   [x] 表单
-   [x] 图表 :bar_chart:
-   [x] 富文本编辑器
-   [x] 图片拖拽/裁剪上传
-   [x] 权限测试
-   [x] 404 / 403
-   [x] 三级菜单
-   [x] 自定义图标
-   [x] 国际化

## 安装步骤

```

npm install         // 安装项目依赖，等待安装完成之后，安装失败可用  yarn install

// 开启服务器，浏览器访问 http://localhost:8080
npm run dev

// 执行构建命令，生成的dist文件夹放在服务器下即可访问
npm run build
```

## 组件使用说明与演示

### vue-schart

vue.js 封装 sChart.js 的图表组件。访问地址：[vue-schart](https://github.com/linxin/vue-schart)

<p><a href="https://www.npmjs.com/package/vue-schart"><img src="https://img.shields.io/npm/dm/vue-schart.svg" alt="Downloads"></a></p>

```html
<template>
    <div>
        <schart class="wrapper" canvasId="myCanvas" :options="options"></schart>
    </div>
</template>

<script>
    import Schart from "vue-schart"; // 导入Schart组件
    export default {
        data() {
            return {
                options: {
                    type: "bar",
                    title: {
                        text: "最近一周各品类销售图",
                    },
                    labels: ["周一", "周二", "周三", "周四", "周五"],
                    datasets: [
                        {
                            label: "家电",
                            data: [234, 278, 270, 190, 230],
                        },
                        {
                            label: "百货",
                            data: [164, 178, 190, 135, 160],
                        },
                        {
                            label: "食品",
                            data: [144, 198, 150, 235, 120],
                        },
                    ],
                },
            };
        },
        components: {
            Schart,
        },
    };
</script>
<style>
    .wrapper {
        width: 7rem;
        height: 5rem;
    }
</style>
```

## License

[MIT](https://github.com/lin-xin/vue-manage-system/blob/master/LICENSE)
