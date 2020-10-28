
# 1. vue首页白屏是什么引起的

一、原因：

单页面应用的 html 是靠 js 生成，因为首屏需要加载很大的js文件(app.js vendor.js)，所以当网速差的时候会产生一定程度的白屏

SPA加载过程：

1. 首先拉取html

2. 解析html, 拉取静态资源（css, js）

3. 解析js 生成html代码（有了大致的结构）

4. ajax 请求，渲染页面

FP: 第一帧数据的像素落点
FCP: 首次内容绘制
FMP: 首次有效绘制
https://liuxuan.blog.csdn.net/article/details/104237256

  === html
    <静态资源>
    <div id="app"></div>     FP

    === 静态资源 css,js
      === 解析js => 生成html   FCP
        <div id="app">
          <div class="head"></div>
          <div class="bodey"></div>
        </div>
        === ajax => 渲染数据   FMP
          <div id="app">
            <div class="head">首页</div>
            <div class="bodey">白屏</div>
          </div>
    


# 1. 什么是骨架屏


# 2. 使用骨架屏的方法（三）

  1. 手写骨架屏 https://segmentfault.com/a/1190000014832185
  2. 插件方式 https://www.jianshu.com/p/0a1b01ad62d6
  https://www.jianshu.com/p/eacac700630e