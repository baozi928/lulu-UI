<demo>
    纵向
</demo>
<template>
    <Breadcrumb class="container" >
        <BreadItem to="/"> 首页  </BreadItem>
        <span >∨</span>
        <BreadItem to="/intro"> 介绍  </BreadItem>
        <span >∨</span>
        <BreadItem to="/install"> 安装 </BreadItem>
        <span >∨</span>
        <BreadItem to="/doc/switch"> Switch组件 </BreadItem>
        <span >∨</span>
        <BreadItem to="/doc/button"> Button组件 </BreadItem>
        <span >∨</span>
        <BreadItem to="/doc/dialog"> Dialog组件 </BreadItem>
        <span >∨</span>
        <BreadItem to="/doc/tabs"> Tabs组件 </BreadItem>
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
<style lang="scss" scoped>
span{
    display: block;
    width: 43px;
    height: 23px;
}

</style>
