# loveEmail

#### 介绍
给妹子发送爱心邮件，捕获其芳心

#### 软件架构
软件架构说明


#### 安装教程

1.  npm install // 下载依赖包
2.  node main.js // 启动项目

#### 使用说明

1. 修改相识日期

   ```javascript
   // 认识的时间 2019-03-01
   const meet = new Date("2019-03-01");
   ```

2.  发件邮箱设置

    ```javascript
    // 使用默认SMTP传输，创建可重用邮箱对象
    let transporter = nodemailer.createTransport({
        host: "smtp.163.com",
        port: 465,
        secure: true, // 开启加密协议，需要使用 465 端口号
        auth: {
            user: "***@163.com", // 用户名
            pass: "***" // 客户端授权密码
        }
    });
    ```

3.  发件邮箱数据设置

    ```javascript
    // 设置电子邮件数据
    let mailOptions = {
        from: '"帅气的小哥哥" <***@163.com>', // 发件人邮箱
        to: "***@**.com", // 收件人列表
        subject: "这个一封充满爱的邮件", // 标题
        html: html // html 内容
    };
    ```

4.  启动项目就行了
