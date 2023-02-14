<demo>
    示例
</demo>
<template>
 <Breadcrumb class="container" >
     <BreadItem to="/"> 首页  </BreadItem>
     <BreadItem to="/doc/intro"> 介绍  </BreadItem>
     <BreadItem to="/doc/install"> 安装 </BreadItem>
     <BreadItem to="/doc/switch"> Switch组件 </BreadItem>
     <BreadItem to="/doc/button"> Button组件 </BreadItem>
     <BreadItem to="/doc/dialog"> Dialog组件 </BreadItem>
     <BreadItem to="/doc/tabs"> Tabs组件 </BreadItem>
     <BreadItem to="/doc/progress"> Progress组件 </BreadItem>
     <BreadItem to="/doc/Tooltip"> Tooltip组件 </BreadItem>
     <BreadItem to="/doc/breadcrumb"> Breadcrumb组件 </BreadItem>
     <BreadItem to="/doc/Pagination"> Pagination组件 </BreadItem>
 </Breadcrumb>
</template>


<script>
import BreadItem from '../lib/BreadItem.vue'
import Breadcrumb from '../lib/Breadcrumb.vue'
export default {
  components: { BreadItem, Breadcrumb },
}
</script>
<style lang="scss" scoped>
h3 {
  font-size: 20px;
  margin-bottom: 15px;
}
</style>
