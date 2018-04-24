<template>
    <ul class="roseList">
            <li class="roseLi" v-for="item in productList" :key="item.index">
                <div class="temp">
                    <img :src="item.headImg" :style="{height:imgHeight}"/>
                    <div class="tit">{{item.title}}</div>
                    <div class="bottom">
                        <img src="http://file.40017.cn/touchweixinqq/indiana/img/icon_flower_homepage__fulishangcheng_rest.png"></img>
                        <div class="left">{{item.rose}}</div>
                    </div>
                </div>
            </li>
    </ul>
</template>

<script>
    export default{
        name:'ProductList',
        props:{
            productList:Array,
            imgHeight:String
        }
    }
</script>

<style>
.roseList {
    padding-left: 15px;
    padding-bottom:50px;
    overflow: hidden;
}
.roseLi {
    float: left;
    width: 50%;
    padding-right: 15px;
    margin-bottom: 10px;
    box-sizing: border-box;
}
.roseLi .temp {
    border: 1px solid #e3e3e3;
    padding:5px 0;
    text-align:left;
}
.roseLi img {
    width: 100%;
}
.roseLi .tit {
    display: -webkit-box;
    -webkit-box-orient: vertical;
    overflow: hidden;
    text-overflow: ellipsis;
    word-break: break-all;
    -webkit-line-clamp: 1;
    font-size: 12px;
    color: #333;
    height:26px;
    line-height:34px;
    padding: 0 10px;

}
.roseLi .bottom {
    display: -webkit-box;
    -webkit-box-align: center;
    font-size: 16px;
    color: #333;
    margin-top: 5px;
    padding: 0 10px;
}
.roseLi .bottom img {
    display: block;
    -webkit-box-flex: 0;
    width: 20px;
    height: 20px;
    margin-right: 5px;
}
.roseLi .bottom .left {
    -webkit-box-flex: 1;
    padding-right: 20px;
    color: #333;
    font-size: 12px;
}

</style>
