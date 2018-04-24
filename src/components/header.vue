<template>
     <div class="fortune">
        <a class="left">
            <img class="im-l" src="http://file.40017.cn/touchweixinqq/indiana/img/icon_diamond_homepage_fulishangcheng_rest.png" />
            <div class="diamond">{{coins.diamond}}</div>
            <img class="im-l" src="http://file.40017.cn/touchweixinqq/indiana/img/icon_flower_homepage__fulishangcheng_rest.png" />
            <div class="rose">{{coins.rose}}</div>
            <div class="add">
                <img class="im-r" src="http://file.40017.cn/touchweixinqq/indiana/img/icon_indicator_add_fulishangcheng_rest2.png" />
            </div>
        </a>
        <div class="right">
            如何获钻
            <img class="im-r" src="http://file.40017.cn/touchweixinqq/indiana/img/icon_indicator_click_problem_fulishangcheng_rest2.png" />
        </div>
    </div>
</template>
<script>
    export default{
        name:'Header',
        props:{
            coins: Object
        }
    }
</script>
<style>
.fortune {
    padding: 0 15px;
    overflow: hidden;
    font-size: 10px;
    position: fixed;
    top: 0;
    left: 0;
    z-index: 100;
    width: 100%;
    background:rgba(0,0,0,.5);
    box-sizing: border-box;
}
.fortune .left {
    float: left;
    border-radius: 20px;
    padding-right: 5px;
    color: #fff;
    height: 35px;
    display: -webkit-box;
    -webkit-box-align: center;
}
.fortune .left>div {
    padding-right: 10px;
    font-size: 12px;
}
.fortune img {
    width: 20px;
    height: 20px;
      display: block;
    -webkit-box-flex: 0;
}
.fortune .left .im-r{
    width: 16px;
    height: 16px;
}
.fortune .im-l {
    margin-right: 5px;
    display: block;
}
.fortune .right {
    float: right;
    color: #fff;
    font-size: 12px;
    height: 35px;
    display: -webkit-box;
    -webkit-box-align: center;
}
.fortune .right img {
    margin-left: 5px;
    display: block;
    width: 16px;
    height: 16px;
}

</style>