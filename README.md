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

1. git init <br>
2. git add .  （一定注意add后面的 . 前后要有空格）<br>
3. git commit -m 'react' <br>
4. git remote add origin https://github.com/JEFT-hai/gallery-by-react <br>
5. git pull origin master <br>
6. git push -u origin master <br>
7. git subtree push --prefix=dist origin gh-pages 推送到Github提供的静态文件访问上 <br>
8. 访问http://jeft-hai.github.io/gallery-by-react/ <br>

#### 知识点

1. 
