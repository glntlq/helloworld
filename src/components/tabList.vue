<template>
   <div class="header">
        <div v-for="(item, index) in typeList"
          :key="item.index"
          class="h-item"
          :class="[index==selected?'active':'']"
          @click="selectType(index)">
        {{item}}
        </div>
    </div>
</template>
<script>
  export default{
    name:'tabList',
    props:{
      selected:{
        type:Number,
        default:0
      },
      typeList:{
        type:Array,
        default:['测试','测试']
      }
    },
    methods:{
      selectType(index){
        this.$emit('selectType',index);
      }
    }
  }
</script>
<style scoped>
.header{
    background: #fff;
    display: -webkit-box;
    -webkit-box-align: center;
    padding: 0 10px;
    height: 42px;
}
.header .h-item{
    -webkit-box-flex: 1;
    width: 0%;
    text-align: center;
    font-size: 14px;
    color: #666;
    line-height: 40px;
}
.header .h-item.active{
    color: #23beae;
    border-bottom: 2px solid #23beae;
}
</style>
