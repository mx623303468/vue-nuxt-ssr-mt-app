# vue-ssr-mt
## 技术栈
  vue + vue-router + vuex + axios + element-ui + nuxt + koa + mongodb + redis
## 环境准备
  - node | 8.12.0
  - vue | 2.5.17
  - npm | 6.4.1
  - webpack | 4.19.1
  - nuxt | 2.0.0

## 辅助工具
  - mongoDB 数据库
  - Robo 3T 数据库可视化工具
  - Redis 

## 项目初始化
  - 使用 nuxt 提供的脚手架 `create-nuxt-app`
    - 确保安装了npx（npx在NPM版本5.2.0默认安装了）：`$ npx create-nuxt-app <项目名>` 或者 `$ yarn create nuxt-app <项目名>`

    - 脚手架会给一些选项
      1. `Project name (项目名) | 项目名称`: 项目名称

      2. ` Project description | 项目描述`: 项目描述

      3. `Use a custom server framework | 在集成的服务器端框架之间进行选择`: Koa

      4. `Use a custom UI framework | 选择您喜欢的UI框架`: Element UI

      5. `Choose rendering mode | 选择你想要的Nuxt模式 (Universal or SPA)`: Universal

      6. `Use axios module | 添加 axios module`: yes

      7. `Use eslint | 添加 EsLint`: yes

      8. `Use prettier | 添加 Prettier`: yes

      9. `Author name | 作者名称`：author

      10. `Choose a package manager | 选择包管理器 （npm OR yarn）`：npm 

    - 项目初始化完成，如果有 npm WARN ，根据提示安装对应依赖。
    - 在项目根目录，启动项目。

      ```shell
        To get started:

          cd test-nuxt-app
          npm run dev

        To build & start for production:

          cd test-nuxt-app
          npm run build
          npm start
      ```

## 配置更改
  - 此时，在 `server` 目录下的文件中，看到使用的是 `require`,说实话这个有点丑，我想用ES6的 `import` 方式，却发现不行。那么就要改造一下了
      - 首先安装babel-cli脚手架
      - 在package.json里在 `dev` `start` 末尾加上`--exec babel-node`
      - 在根目录下创建一个`.babelrc`文件在里面编辑
        ```JSON
          {
            "presets": ["env"]
          }
        ```
      - 在安装一下配置 `npm i -D babel-cli babel-preset-env`
      - 重启项目，就可以使用了。
  - 因为要使用 `sass`， 所以需要安装 `npm i sass-loader node-sass`
