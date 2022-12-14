vue3工程的目录结构和vue2工程的目录结构是一致的，但是文件内容存在一定的变化

目录结构：
    node_modules      用来存放我们项目中的各种依赖
    public            用来存放静态资源
        index.html    模板文件，生成项目的入口文件
        favicon.ico   图标文件
    src               源码目录
        assets        用来存放各种静态文件
        components    用来存放公共组件，button组件、header组件...
            HelloWorld.vue
        App.vue       主vue模块，项目的主组件，所有的页面都是在App.vue下面进行切换的
        main.js       入口文件
    .gitignore        配置git上传的时候，需要忽略的文件的格式
    babel.config.js   ES6转ES5相关的配置
    jsconfig.json     你的工作空间中出现了jsconfig.json，js体验会得到改进
    package.json      项目的基本信息：项目信息、依赖、脚本
    package-lock.json 锁版本
    vue.config.js     完成webpack的一些特殊的配置

文件的变化：
    main.js