1、建立工程目录

　　src:使用ES6语法编写的JS文件；

　　dist:使用Babel转换成ES5的文件，在项目引用的时候引用的是这个文件夹里边的JS文件

2、初始化项目 

　　npm init -y  

　　-y是指表示全部默认，不需要一个一个敲回车

3、全局安装Babel-cli   

　　

```
npm install -g babel-cli
```

 

4、本地安装babel-preset-es2015 和 babel-cli

　　

```
npm install --save-dev babel-preset-es2015 babel-cli
```

 

5、新建.babelrc

　　

```
{
    "presets":[
        "es2015"
    ],
    "plugins":[]
}
```

6、输入终端转换命令

　　

```
babel src/index.js -o dist/index.js
```

***简化终端命令

　　修改package.json文件中的scripts,修改后为

[![复制代码](https://common.cnblogs.com/images/copycode.gif)](javascript:void(0);)

```
{
  "name": "es6",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "build": "babel src/index.js -o dist/index.js"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "babel-cli": "^6.24.1",
    "babel-preset-es2015": "^6.24.1"
  }
}

然后运行 npm run build 进行转换
```

