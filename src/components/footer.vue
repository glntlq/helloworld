<template>
      <div class="menu-box">
        <a class="menu-d">
            <img src="http://file.40017.cn/touchweixinqq/indiana/img/icon_store_homepage_diamond_rest.png"></img>
            <div>钻石乐园</div>
        </a>
        <a class="menu-d">
            <img src="http://file.40017.cn/touchweixinqq/indiana/img/icon_store_homepage_green_flower_rest.png"></img>
            <div class="hlight">玫瑰商城</div>
        </a>
        <a class="menu-d">
            <img src="http://file.40017.cn/touchweixinqq/indiana/img/icon_store_homepage_mine_rest.png"></img>
            <div>我的</div>
        </a>
    </div>
</template>
<script>
</script>
<style>
.menu-box {
    display: box;
    display: -webkit-box;
    height: 55px;
    padding: 0 5px;
    font-size: 0;
    background: #fff;
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: 99;
    border-top: 1px solid #e3e3e3;
}
.menu-d {
    display: block;
    box-flex: 1;
    -webkit-box-flex: 1;
    width: 0;
    text-align: center;
}

.menu-d > img {
    padding-top: 7px;
    width: 24px;
    height: 24px;
}

.menu-d > div.hlight {
    color: #23beae;
}

.menu-d > div {
    padding-top: 1px;
    font-size: 12px;
    color: #333;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}
</style>
