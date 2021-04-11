# vue

- webpack 安装

  ```
  <!--webpack 安装-->
  npm i webpack@4.44.1 -g

  <!--安装webpack-cli-->
  npm install -g webpack-cli@3.3.12
  # OR
  yarn global add webpack-cli@3.3.12
  <!-- 卸载 -->
  npm uninstall -g webpack
  npm uninstall -g webpack-cli
  ```

- webpack
  ```
  webpack -v:查看webpack版本
  webpack-cli -v:查看webpack-cli版本
  ```
- es6 的解析
  ```
  安装：
  yarn add @babel/core @babel/preset-env babel-loader --dev
  注解：@babel/preset-env：es6相关
  代码：
  webpack.config.js:
  module:{
        rules:[
            {
                test:'/\.js$/',use:'babel-loader'
            }
        ]
    }
  .babelrc:
  {
      "presets": [
          "@babel/preset-env"
      ]
  }
  ```
  vue 的解析
  ```
  yarn add vue-loader vue-template-compiler --dev
  yarn add vue
  ```
- css 解析

  ```
  npm i style-loader css-loader -D
  注释：style-loader:把css通过style的方式插入到html的head中；
  css-loader：解析css[因为webpack不能解析css]
  module:{
        rules:[
            {
                test:'/\.js$/',use:'babel-loader'
            },
            {
                test:'/\.css$/',use:[
                    'style-loader',
                    'css-loader'
                ]
            }
        ]
    }
  npm i mini-css-extract-plugin -D
  注解: 将css提取成一个css文件，通过link方式插入到html的head中，与style-loader对立(不能同时使用)；
  相关代码：

  ```

- less 相关解析
  ```
  yarn add less less-loader --dev
  或者
  npm i less less-loader -D
  相关代码：
  {
      test:'/\.less$/',use:[
          'style-loader',
          'css-loader',
          'less-loader'
      ]
  }
  ```
- SCSS 相关解析
  ```
  yarn add node-sass sass-loader --dev
  相关代码：
  {
      test:'/\.scss$/',use:[
          'style-loader',
          'css-loader',
          'sass-loader'
      ]
  }
  ```
- px 转换为 rem 相关解析
  ```
  yarn add px2rem-loader --dev
  yarn add lib-flexible --dev
  注解：
  相关代码：
  ```
- css3 的属性增强添加前缀 相关解析

  ```
  yarn add postcss-loader autoprefixer --dev
  注解：
  相关代码：
  ```

- 图片或字体 相关解析

  ```
  yarn add file-loader --dev
  或者
  yarn add url-loader --dev
  注解：url-loader:可以通过limit：10240；设置图片小于10k的图片转换为base64的方式进行；
  相关代码：
  module:{
        rules:[
               {
                  test:'/\.(jpg|jpeg|png|gif)$/',
                  use:[
                      {
                          loader:'url-loader',
                          options:{
                              limit:10240
                          }
                      }
                  ]
                }
        ]
  }
  ```

- 压缩 相关解析

  ```
  <!-- css压缩 -->
  yarn add optimize-css-assets-webpack-plugin cssnano  --dev
  <!-- html的压缩 -->
  yarn add html-webpack-plugin  --dev
  <!-- js压缩 webpack4以及内置了uglify-webpack-plugin 插件处理js的压缩,不用再另外增加 -->
  相关代码：
  ```

- 静态资源内联 相关解析

  ```
  <!-- 资源内联 -->
  yarn add raw-loader  --dev
  相关代码：
  ```

- 自动清理构建目录 dist 相关解析

  ```
  <!-- 资源内联 -->
  yarn add clean-webpack-plugin  --dev
  相关代码：
  const {CleanWebpackPlugin} = require('clean-webpack-plugin');

  plugins:[
        new CleanWebpackPlugin()
    ]
  ```

- html 模板

  ```
  const HtmlWebpackPlugin = require('html-webpack-plugin')
  plugins:[
      new HtmlWebpackPlugin({
          template:'./public/index.html',
          filename:'index.html',
          minify:{
              html5:true,
              minifyCSS:true,
              minifyJS:true
          }
      })
  ]

  ```

- 多页面打包

  ```
  <!-- 资源内联 -->
  yarn add glob  --dev
  相关代码：


  ```
test
# npm

- `npm install -g npm@latest` ：npm 安装到最新版本
- `npm install -g cnpm --registry=https://registry.npm.taobao.org`:
