# MyRep

<style type="text/css">
        html,body,div,input,ul,li,a{margin:0;padding:0;}
        body{font-family: "microsoft yahei";}
        input{border:none;outline: none;}
        a{text-decoration:none;}
        ul{list-style: none;}
        #div1{position:relative;margin:100px auto;padding:20px 25px;width:686px;height:480px;background-color: #efefef;}
        #div1>span{font-size:24px;font-weight:800; }
        #div1>input{border:1px solid #de4200;background-color: #ff0000;height:38px;width:98px;color:#fff;box-shadow: 1px 1px 0 #efbd6b,-1px -1px 0 #efbd6b;font-weight:800; cursor: pointer;}
        #div2{margin-top:25px;height:100px;width:100px;border:4px solid #000;background-color: #fff;}
        #cover{position:absolute;top:0;left:0;width:686px;height:460px;padding:30px 25px;background-color: rgba(0,0,0,.3);display: none;}
        .wrap{margin:218px 0 0 345px;padding:15px 32px;width:236px;height:170px;background-color: #fff;border:20px solid #9c949c;}
        .wrap a{font-size: 12px; color:#808080;display: inline-block;height:30px;width:34px;line-height: 30px;text-align: center;background-color: #efefef;border:1px solid #c0c0c0;margin-left:5px;}
        .wrap a:hover{color:#000;}
        .wrap .color{height:30px;line-height: 30px;}
        .wrap .color a{font-size: 12px; color:#fff;}
        .wrap .color a:hover{font-size: 12px; color:#000;}
        ul li{height:34px;line-height: 34px;margin-bottom: 10px;}
        li .red{background-color: red;}
        li .yellow{background-color: yellow;}
        li .blue{background-color: blue;}
        #reset{margin:20px auto;width:144px;}
        #reset input{height:30px;width:60px;line-height:30px;background-color: #002952;color:#fff; cursor: pointer;margin-left:12px;}
    </style>

<div id="div1">
    <span>请为下面的DIV设置样式：</span><input type="button" value="点击设置" id="btn1"/>
    <div id="div2"></div>
    <div id="cover">
        <div class="wrap">
            <ul id="ul">
                <li class="color"><span>请选择背景色：</span><a href="javascript:;" class="red">红色</a><a href="javascript:;" class="yellow">黄色</a><a href="javascript:;" class="blue">蓝色</a></li>
                <li><span>请选择宽(px)：</span><a href="javascript:;">200</a><a href="javascript:;">300</a><a href="javascript:;">400</a></li>
                <li><span>请选择高(px)：</span><a href="javascript:;">200</a><a href="javascript:;">300</a><a href="javascript:;">400</a></li>
            </ul>
            <div id="reset">
                <input type="button" value="恢复" id="btn2"/><input type="button" id='btn3' value="确定"/>
            </div>
        </div>
    </div>
</div>

<script type="text/javascript">
    var div2=document.getElementById('div2');
    var btn1=document.getElementById('btn1');
    var btn2=document.getElementById('btn2');
    var btn3=document.getElementById('btn3');
    var cover=document.getElementById('cover');
    var ul=document.getElementById('ul');
    var li1=ul.getElementsByTagName('li')[0];
    var li2=ul.getElementsByTagName('li')[1];
    var li3=ul.getElementsByTagName('li')[2];
    var links1=li1.getElementsByTagName('a');
    var links2=li2.getElementsByTagName('a');
    var links3=li3.getElementsByTagName('a');
    btn1.onclick=function(){
        cover.style.display='block';
    };
    btn3.onclick=function(){
        cover.style.display='none';
    };

    for(var i=0;i<links1.length;i++){
        links1[i].index=i;
        links1[i].onmouseover= function () {
            div2.style.backgroundColor=this.className;
        };
    }
    for(var i=0;i<links2.length;i++){
        links2[i].index=i;
        links2[i].onmouseover= function () {
            div2.style.width=this.innerHTML+"px";
        };
    }
    for(var i=0;i<links3.length;i++){
        links3[i].index=i;
        links3[i].onmouseover= function () {
            div2.style.height=this.innerHTML+"px";
        };
    }
    btn2.onclick=function(){
        div2.style.height=100+'px';
        div2.style.width=100+'px';
        div2.style.backgroundColor='#fff';
    };
</script>
