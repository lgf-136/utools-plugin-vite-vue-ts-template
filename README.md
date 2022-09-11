# Vue 3 + TypeScript + Vite

This template should help get you started developing with Vue 3 and TypeScript in Vite. The template uses Vue 3 `<script setup>` SFCs, check out the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar)

## Type Support For `.vue` Imports in TS

Since TypeScript cannot handle type information for `.vue` imports, they are shimmed to be a generic Vue component type by default. In most cases this is fine if you don't really care about component prop types outside of templates. However, if you wish to get actual prop types in `.vue` imports (for example to get props validation when using manual `h(...)` calls), you can enable Volar's Take Over mode by following these steps:

1. Run `Extensions: Show Built-in Extensions` from VS Code's command palette, look for `TypeScript and JavaScript Language Features`, then right click and select `Disable (Workspace)`. By default, Take Over mode will enable itself if the default TypeScript extension is disabled.
2. Reload the VS Code window by running `Developer: Reload Window` from the command palette.

You can learn more about Take Over mode [here](https://github.com/johnsoncodehk/volar/discussions/471).

[Vite 世界指南（带你从 0 到 1 深入学习 vite）](https://www.bilibili.com/video/BV1GN4y1M7P5?p=7&spm_id_from=pageDriver&vd_source=6cecd1f17a6c0ef08a944dd92199a516)

https://blog.csdn.net/mouday/article/details/126336560
https://www.bilibili.com/video/BV1Pd4y1S7Mp/?spm_id_from=333.788.recommend_more_video.2&vd_source=6cecd1f17a6c0ef08a944dd92199a516

npm i -D postcss postcss-cli postcss.parts browserslist autoprefixer postcss-preset-env stylelint stylelint-config-standard stylelint-config-prettier postcss-pxtorem

npm i -D postcss postcss-cli browserslist autoprefixer postcss-preset-env stylelint stylelint-config-standard stylelint-config-prettier postcss-pxtorem less sass mockjs vite-plugin-html vite-plugin-mock vite-plugin-utools

npm i -D postcss postcss-cli browserslist autoprefixer postcss-preset-env stylelint stylelint-config-standard stylelint-config-prettier postcss-pxtorem less sass mockjs vite-plugin-html vite-plugin-mock vite-plugin-utools @types/node ts-node utools-api-types

npx postcss main.css -o dist.css
npx postcss main.css -o dist.css -u autoprefixer
npx postcss main.css -o dist.css -u autoprefixer --no-map

https://github.com/uTools-Labs/utools-api-types

uTools API 代码提示
第一步

npm install utools-api-types --save-dev
第二步 配置 tsconfig.json

{
"compilerOptions": {
"types": [
"utools-api-types"
]
}
}
API 代码示例
// 默认浏览器打开网页
window.utools.shellOpenExternal('https://u.tools')

// 在资源管理器中显示文件
window.utools.shellShowItemInFolder('d:\\test')

// ubrowser 网页自动化
window.utools.ubrowser.goto('https://cn.bing.com')
.value('#sb_form_q', 'uTools')
.click('#sb_form_go')
.run({ width: 1000, height: 600 })

// 获取当前浏览器 URL
window.utools.getCurrentBrowserUrl()

// 值键对方式存储数据
window.utools.dbStorage.setItem('key', 'value')

// 执行截图
window.utools.screenCapture((imagebase64) => {
// 截图完的回调
})

// 执行取色
window.utools.screenColorPick(({ hex, rgb }) => {
// 取色完的回调
})
