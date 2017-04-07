# hello-world
DDNS
<!doctype html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="icon" href="./images/favicon.ico" type="image/gif">
    <link rel="stylesheet" href="./css/index.css">
    <link rel="stylesheet" href="https://cdn.rawgit.com/ElemeFE/mint-ui/master/lib/style.css">
    <script src="https://cdn.jsdelivr.net/vue/latest/vue.js"></script>
    <script src="https://cdn.jsdelivr.net/vue.resource/1.2.1/vue-resource.min.js"></script>
    <script src="https://cdn.rawgit.com/ElemeFE/mint-ui/master/lib/index.js"></script>
    <script src="./js/all.js"></script>
    <title>动态域名解析</title>
</head>
<body>
<div class="body" :style="heightObject">
    <div class="header">
        <div>
            <img :src="header.imgSrc" alt="介夫子logo">
        </div>
    </div>
    <div class="form" @keyup.enter="login">
        <div>
            <div>
                <input type="text"  v-model="account" placeholder="请输入账户">
            </div>
            <div id="passwordInput">
                <input type="password" v-model="password11" placeholder="请输入密码">
            </div>
            <div class="submit">
                <input type="submit"  value="登 录" @click="login" :disabled="disabled">
            </div>
        </div>
    </div>
</div>
<script>
     var lodin = new Vue({
        el:'.body',
        data:{
            heightObject:{
                height:''
            },
            header:{
                imgSrc:'./images/alyDDNS.jpg'
            },
            disabled:false,
            account:'',
            password11:''
        },
        created:function () {
            //页面高度
            this.heightObject.height = document.documentElement.clientHeight+'px';
        },
        methods: {
            login:function () {
                var _self = this;
                _self.disabled = true;
                //账号不能为空
                if(_self.account == ''){
                    _self.$messagebox.alert('账号不能为空').then(function () {
                    });
                    _self.disabled = false;
                    return false;
                }
                //密码不能为空
                if(_self.password11 == ''){
                    _self.$messagebox.alert('密码不能为空').then(function () {

                    });
                    _self.disabled = false;
                    return false;
                }
                var url =''+domainl+'/account/login';
                var data = {};
                data.account = _self.account;
                data.password = _self.password11;
                console.log(data);
                //跨域
                Vue.http.interceptors.push(function(request, next){
                    request.credentials = true;
                     next()
                 });
                //提取后台信息
                _self.$http.post(url,data).then(function (data){
                    var dataNew = data.body;
                    _self.disabled = false;
                    if(dataNew.status == 200){
                        //缓存账户名
                        localStorage.name =  _self.account;
                        window.location.href = './html/task.html?backurl='+window.location.pathname+''
                    }else {
                        var message =  dataNew.message;
                        //登录失败后弹出对话框
                        _self.$messagebox.alert(message).then(function () {
                            _self.disabled = false;
                        });
                    }
                },function (response) {
                    _self.disabled = false;
                    console.log(response);
                });
            }
        }
    });
</script>
</body>
</html>
