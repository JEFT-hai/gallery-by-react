### gallery-by-react

#### 安装运行 使用yoman、webpack

1. npm install yo -g <br>
2. npm install generator-react-webpack -g <br>
3. yo react-webpack gallery-by-react 自动生成项目 <br>
4. 运行 node server.js <br>
5. npm install autoprefixer-loader --save-dev <br>
6. 编辑 Main.js 开始项目 <br>
7. 打包 npm run dist <br>

#### 发布项目 <br>

###### 注意

发布时：index.html中要直接引用的文件地址<br>
发布时：图片引用地址要更改 <br>

1. git init <br>
2. git add .  （一定注意add后面的 . 前后要有空格）<br>
3. git commit -m 'react' <br>
4. git remote add origin https://github.com/JEFT-hai/gallery-by-react <br>
5. git pull origin master <br>
6. git push -u origin master <br>
7. git subtree push --prefix=dist origin gh-pages 推送到Github提供的静态文件访问上 <br>
8. 访问http://jeft-hai.github.io/gallery-by-react/ <br>

#### 知识点

1. 图片的信息存在imageDatas.json中 <br>
2. 翻转图片：.img-back 先翻转180度，这样就到了背面，点击时父元素翻转180度，这样子元素就是360度，就朝上了。<br>
   父元素 .img-figure.is-inverse{transform:translate(320px) rotateY(180deg);}<br>
   子元素 .img-back{transform:rotateY(180deg) translateZ(1px);} （translateZ(1px)是为了兼容性）<br>
   改进翻转画面：.img-sec （perspective:600px;）<br>
   .img-figure  <br>
     　{ <br>
      　transform-origin: 0 50% 0; <br>
      　transform-style:preserve-3d; <br>
      　transition:transform .6s ease-in-out,left .6s ease-in-out,top .6s ease-in-out; <br>
     　} <br>
3. react创建组件 class AppComponent extends React.Component {}
4. react获取DOM节点 let stageDOM = ReactDOM.findDOMNode(this.refs.stage) ref="stage"。
