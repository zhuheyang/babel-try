# babel-try

之前在项目中没有使用过babel, 一般都是使用Expres或者Angular的框架直接上.对这些工具的操作并不熟悉.使用Express时并不会ES6的语法, 使用Angular时又不用操心打包编译.则Webpack就更加没有接触过相关了.
babel的具体使用场景与使用方法, 可以参考Youtube上面的一个up主的视频,至少能对他的基本使用有个大概的了解.
Morgan说过的, 跟被人学最快, 跟书本学其次, 自学最慢了!

#### babel的改变

现在babel都集合到一个core中了, 如同redux的改变一般.
则下载依赖时,都是首先下载"@babel/core": "^7.0.0-beta.36",之后才是下载preset-env相关了.
则不是之前, 也即尚未更新的官网中所说: 先下载babel-cli, 之后再下载babel-preset-env
新的babel/babel库中有给出几种不同浏览器环境对应的babel设置, 例如不能使用module等等. 包括IE10, safari>8等等这种常见的开发环境.
还有Node6.0等等.

#### 对应.babelrc的改变

刚开始使用, 只能按照官网的, 设置最简单的

```json
{ "preset" : "env" }
```

来简单运行着先.
关于目前最新的babel/core的用法的话, 先悠着点吧!
给出一个示例为:

```json
{
  "presets": [
    ["@babel/preset-env", {
      "targets": {
        "browsers": ["last 2 versions", "safari >= 7"]
      }
    }]
  ]
}
```
