# v2-template-bancheng

## 模板文件配置

```javascript
Vue CLI v5.0.8
? Please pick a preset: Manually select features
? Check the features needed for your project: Babel, Router, CSS Pre-processors, Linter
? Choose a version of Vue.js that you want to start the project with 2.x
? Use history mode for router? (Requires proper server setup for index fallback in production) No
? Pick a CSS pre-processor (PostCSS, Autoprefixer and CSS Modules are supported by default): Sass/SCSS (with dart-sass)
? Pick a linter / formatter config: Airbnb
? Pick additional lint features: Lint on save
? Where do you prefer placing config for Babel, ESLint, etc.? In dedicated config files
```

手机端兼容处理

`npm install postcss-px-to-viewport --save-dev`

`vue.config.js`同级创建`postcss.config.js`文件

配置处理

```javascript
module.exports = {
  plugins: {
    // ...
    'postcss-px-to-viewport': {
        // 要转化的单位
      unitToConvert: 'px',
        // 设计稿视口宽度
      viewportWidth: 375,
        // 转换后保留的精度
      unitPrecision: 5,
        // 希望的视口单位
      viewportUnit: 'vw',
        // 字体使用的视口单位
      fontViewportUnit: 'vw',
    },
  },
};
```



