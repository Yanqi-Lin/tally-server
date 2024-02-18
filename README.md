### 后端选型
Egg.js
MySQL

### 注册和登录 —— JWT用户鉴权
JSON Web Tokens（JWT）： JWT 是一种用于在不同系统之间安全传递信息的开放标准。它常用于在客户端和服务器之间传递身份信息，包括用户身份和权限。

我们把获取到的 userInfo 中的 id 和 username 两个属性，通过 app.jwt.sign 方法，结合 app.config.jwt.secret 加密字符串，生成一个 token。这个 token 会是一串很长的加密字符串，类似这样 dkadaklsfnasalkd9a9883kndlas9dfa9238jand 的一串密文。

### 用户信息修改 —— 实现上传图片
1、首先我们需要在前端调用上传接口，并将图片参数带上。

2、在服务端接收前端传进来的图片信息，信息中含有图片路径信息，我们在服务端通过 fs.readFileSync 方法，来读取图片内容，并存放在变量中。

3、找个存放图片的公共位置，一般情况下，都会存放至 app/public/upload，上传的资源都存在此处。

4、通过 fs.writeFileSync 方法，将图片内容写入第 3 步新建的文件夹中。

5、最后返回图片地址，基本上图片地址的结构是 host + IP + 图片名称 + 后缀。

### 账单及其相关接口

### API文档

### 优化升级

1. piGo + gitHub 自建图床
2. 将密码通过 md5 或者其他的形式加密

# tally-server



## QuickStart

<!-- add docs here for user -->

see [egg docs][egg] for more detail.

### Development

```bash
npm i
npm run dev
open http://localhost:7001/
```

### Deploy

```bash
npm start
npm stop
```

### npm scripts

- Use `npm run lint` to check code style.
- Use `npm test` to run unit test.

[egg]: https://eggjs.org
