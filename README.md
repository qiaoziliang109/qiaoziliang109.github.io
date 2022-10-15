# qiaoziliang109.github.io
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>注册页面</title>
    <link rel="stylesheet" href="css/Register.css">
    <!--导入Vue-->
    <script src="js/vue.js"></script>
    <!--导入axios-->
    <script src="https://cdn.staticfile.org/axios/0.18.0/axios.min.js"></script>
</head>
<body id="body">
<!-- 登入模块 -->
<div id="RegisterShow">
    <!-- 登入框左侧图片 -->
    <img id="imgDiv" src="imgs/RegisterBgImg.png">
    <!-- 登入输入框整体 -->
    <div id="RegisterDiv">
        <form action="" id="form">
            <!-- 输入框模块 -->
            <h1 id="RegisterMsgDiv">用户注册</h1>
            <a id="login" href="http://localhost:8080/Login.html">已有账号？直接登录</a>
            <input id="username" name="username" type="text" placeholder="输入学号" @blur="BlurId" v-model="register.student.StuId">
            <div id="errorMsg">{{IdErrorMsg}}</div>
            <input id="password" name="password" type="password" placeholder="输入登录密码" v-model="register.student.password" @blur="BlurPd"><br>
            <input id="checkpassword" name="checkpassword" type="password" placeholder="再次输入登录密码" v-model="checkPassword" @blur="BlurPd"><br>
            <div id="errorMsg">{{PdErrorMsg}}</div>
            <div id="checkCodeDiv">
                <input id="checkCode" type="text" placeholder="请输入验证码" v-model="register.checkCode">
                <img id="checkCodeImg" src="/checkCodeServlet">
                <!-- <a href="#" id="changeImg">看不清？</a> -->
            </div>
            <!-- <p id="errorMsg">验证码错误!</p> -->
            <div id="errorMsg">{{ RegisterErrorMsg }}</div>
            <!-- 按钮模块 -->
            <div id="subDiv">
                <input id="registerSub" type="button" value="注册" @click="RegisterSubmit">
            </div>
        </form>
    </div>
</div>
</body>
<!--向后端发送请求的脚本,必须放在后面,先等html标签编译-->
<script src="js/Register.js"></script>
</html>
