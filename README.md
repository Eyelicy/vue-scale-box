# 介绍

> 根据设计稿大小，在不同分辨率下等比例缩放的大屏适配方案

# 如何使用

## 安装

```
    npm install scale-box

    yarn add scale-box
```

## 引用

```
    import ScaleBox from 'scale-box'
```

## 使用及示例

```
    <template>
        <scale-box :width="1920" :height="1080">
        </scale-box>
    </template>

    <script setup>
        import ScaleBox from 'scale-box'
        import 'scale-box/dist/style.css'
    </script>

    <style>
        html,
        body,
        #app {
            width: 100%;
            height: 100%;
        }
    </style>
```

### Slots / 插槽

| 名称    | 说明 | 默认值 |
| ------- | ---- | ------ |
| default | 内容 | 无     |

### Attributes / 属性

| 名称   | 说明         | 默认值 |
| ------ | ------------ | ------ |
| width  | 大屏设计宽度 | 1920   |
| height | 大屏设计高度 | 1080   |

# Vue 3 + Vite

This template should help get you started developing with Vue 3 in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

## Recommended IDE Setup

- [VSCode](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=johnsoncodehk.volar)
