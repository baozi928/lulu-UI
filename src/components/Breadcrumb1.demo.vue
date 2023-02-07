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
     <BreadItem to="/doc/breadcrumb"> Breadcrumb组件 </BreadItem>
 </Breadcrumb>
</template>


<script>
    import {
        BreadItem,Breadcrumb
    } from "../lib/index";
    export default {
        components: { BreadItem, Breadcrumb },
    }

</script>

