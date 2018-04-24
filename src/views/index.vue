<template>
    <div>
      <roseHeader :coins= "coinNum"></roseHeader>
      <div :style="{height:imgHeight}">
        <mt-swipe :auto="0">
            <mt-swipe-item
                    v-for="item in bannerList"
                    :key="item.index">
                <img :src='item.imageUrl'/>
            </mt-swipe-item>
       </mt-swipe>
      </div>
        <div class="rosemall">
            <div class="hd">
                <img src="http://file.40017.cn/touchweixinqq/indiana/img/img_indicator_title_rosestore_fulisahngcheng_rest.png"/>
            </div>
            <tab-list
            :selected="selected"
            :typeList="typeList"
            @selectType="tabSelect"
            ></tab-list>
            <productList
                :product-list="productList"
                :img-height="productHeight"
                v-infinite-scroll="loadMore"
                infinite-scroll-disabled="loading"
                infinite-scroll-distance="10">
            </productList>
        </div>
        <roseFooter></roseFooter>
    </div>
</template>
<script>
import roseHeader from "../components/header";
import productList from "../components/productList";
import roseFooter from "../components/footer";
import tabList from "../components/tabList";
import mockData from "../../static/js/data"
export default {
    components: {
	    roseHeader,
      productList,
      roseFooter,
      tabList,
	},
   data() {
    return {
      imgHeight: "",
      productHeight: "",
      coinNum: {
        diamond: "1000",
        rose: "300"
      },
      bannerList:mockData.bannerList,
      productList:mockData.productList,
      selected:0,
      typeList: ['每日竞猜', '九宫格', '转转转', '猜大小', '抓娃娃'],

    };
  },
  mounted() {
    this.setImgH();
  },
  methods: {
    setImgH(){
        let width = document.body.clientWidth;
        this.imgHeight = width * 300 / 750 + "px";
        let productwidth = (width - 15) / 2 - 15 - 2;
        this.productHeight = productwidth * 420 / 750 + "px";
    },
    loadMore() {
      this.loading = true;
      setTimeout(() => {
        let last = this.productList;
        for (let i = 0; i <= 5; i++) {
          this.productList.push(last[i]);
        }
        this.loading = false;
      }, 1500);
    },
    tabSelect(playLoad){
      this.selected = playLoad;
    },
  }
};
</script>
<style scoped>
.rosemall {
  margin-top: 10px;
  background: #fff;
  padding-bottom: 15px;
}
.rosemall .hd {
  padding-top: 15px;
  padding-bottom: 15px;
  text-align: center;
}
.rosemall .hd img {
  width: 60%;
}
</style>
