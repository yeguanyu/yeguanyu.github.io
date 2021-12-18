<!DOCTYPE html>
<h1>注册 WGY play网站</h1>
<html>
    <head>
        <meta charset="UTF-8">
        <title></title>
        <link rel="stylesheet" type="text/css" href="css/reset.css"/>
        <style type="text/css">
            textarea{
                resize: none;
            }
        </style>
        <script type="text/javascript">
            window.onload=function(){
                var oUser=document.getElementById('username');
                var oPwd=document.getElementById('password');
                var oBtn=document.getElementById('btn');
                oBtn.onclick=function(){
                    var upData=null;
                    var repeat=null;
                    if (oUser.value&&oPwd.value) {
                        if (window.localStorage.getItem('list')) {
                            upData={'username':oUser.value,'password':oPwd.value};
                            var dataJson=window.localStorage.getItem('list');
                            dataJson=eval('('+dataJson+')');
                            for (var i=0;i<dataJson.length;i++) {
                                if (dataJson[i].username==upData.username) {
                                    alert('用户名重复');
                                    repeat=1;
                                }
                            }
                            if (repeat==null) {
                                alert('注册成功');
                                dataJson.push(upData);
                                dataJson=JSON.stringify(dataJson);
                                window.localStorage.setItem('list',dataJson);
                                console.log(window.localStorage.getItem('list'));
                            }
                        } else {
                            upData={'username':oUser.value,'password':oPwd.value};
                            console.log(upData);
                            var data=[];
                            data.push(upData);
                            data=JSON.stringify(data);
                            window.localStorage.setItem('list',data);
                            alert(' 注 册 成 功');
                            console.log(window.localStorage.getItem('list'));
                        }
                    }
                }
            }
        </script>
    </head>
    <body>
        <form action="" method="post">
            用户名：<input type="text" id="username" /><br />
            密码：<input type="password" id="password" /><br />
            <input type="button" id="btn" value="注 册" />
        </form>
    </body>
</html>
<a href="http://w.vaiwan.com/denglu.html" class="button">已有账号可登录</a>
</head>
</head>
</head>

<a href="http://w.vaiwan.com/图片.html" class="button">请勿点击</a>

 <a href="http://w.vaiwan.com/liuyanban.html" class="button">留言板</a>


 <a href="http://w.vaiwan.com/ceshiqi.html" class="button">测试器</a>
