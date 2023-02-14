<template>
    <div @click="go">
        <!-- 上一页 -->
        <button class="prev"
                go="-1"
                :disabled="currentNo === 1"
                :class="{disabled: currentNo === 1}">上一页</button>
        <!-- 第一页 -->
        <button v-show="startEnd.start >= 2"
                :go="1"  >1</button>
        <!-- 省略号 -->
        <span class="[elli]"
              v-show="startEnd.start >= 3">...</span>
        <!-- 中间连续页码 -->
        <button v-for="(item, index) in startEnd.end"
                :key="index"
                :go="item"
                v-show="item >= startEnd.start"
                :class="{checked: item === currentNo}">{{item}}</button>
        <!-- 省略号 -->
        <span class="elli"
              v-show="startEnd.end <= totalPages - 2">...</span>
        <!-- 最后一页 -->
        <button v-show="startEnd.end < totalPages"
                :go="totalPages">{{totalPages}}</button>
        <!-- 下一页 -->
        <button class="next"
                :disabled="currentNo === totalPages"
                :class="{disabled: currentNo === totalPages}"
                go="+1">下一页</button>
    </div>
</template>

<script setup>
    import { computed, ref } from 'vue'

    const props = defineProps({
        // 总数量
        totalItems: Number,
        // 每页的数量
        pageItems: Number,
        // 中间连续页码
        continues: {
            type: Number,
            default: 5
        }
    })

    // 总页数
    const totalPages = computed(() => Math.ceil(props.totalItems / props.pageItems))

    // 当前页码
    let currentNo = ref((totalPages.value > 0) ? 1 : 0)

    // 计算中间连续页码的开始、结束位置
    let startEnd = computed(() => {
        let start = 0, end = 0
        // 总页数不够，那么就不存在中间连续页码的问题了
        if(totalPages.value < props.continues) {
            start = 1
            end = totalPages.value
        } else {
            // 连续页码数量的一半
            const dx = Math.floor(props.continues / 2)
            start = currentNo.value - dx
            end = currentNo.value + dx
            // 判断边界（假如有20页）
            if(start < 1) {
                start = 1
                // 1 2 3 4 5 ... 20
                end = props.continues
            }
            if(end > totalPages.value) {
                end = totalPages.value
                // 1 ... 16 17 18 19 20
                start = totalPages.value - props.continues + 1
            }
        }
        return {start, end}
    })

    /**
     * 跳转页面
     */
    function go(e) {
        const target = e.target || e.srcElement
        if(target.nodeName.toLowerCase() === 'button') {
            const goIndex = target.getAttribute('go')
            // 上一页、下一页
            if(['-1', '+1'].includes(goIndex)) {
                currentNo.value = goIndex - 0 + currentNo.value
                if(currentNo.value < 1) currentNo.value = 1
                if(currentNo.value > totalPages.value) currentNo.value = totalPages.value
            } else {
                currentNo.value = goIndex - '0'
            }
        }
    }


</script>

<style lang="scss" scoped>

    button {
        width: 30px;
        height: 30px;
        margin-right: 10px;
        border: none;
        cursor: pointer;
        border-radius: 5px;
        background-color: #fff;
        font-size: 14px;
        &:hover {
            border: 1px solid #ddd;
        }
    }
    .prev, .next {
        width: 60px;
        height: 30px;
        font-size: 16px;
        color: royalblue;
    }
    .checked {
        background-color: royalblue;
        color: #fff;
        &:hover {
            border: none;
        }
    }
    .disabled {
        color: #aaa;
        cursor: default;
        &:hover {
            border: none;
        }
    }
    .elli {
        margin-right: 10px;
        color: #aaa;
        cursor: default;
    }
</style>