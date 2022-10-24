<template>
    <div class="progress-circle">
        <svg :width="size" :height="size" viewBox="0 0 100 100">
            <circle r="50"  cx="50" cy="50" fill="transparent" class="progress-background"></circle>
            <circle r="50" cx="50" cy="50" fill="transparent" class="progress-bar" :stroke-dasharray="dashArray" :stroke-dashoffset="dashOffset"></circle>
        </svg>
    </div>
</template>

<script>
    export default {
        props:{
            size:{
                type:Number,
                default:100
            },
            percent:{
                type:Number,
                default:0.5
            }
        },
        data(){
            return{
                dashArray:Math.PI * 2 * 50
            }
        },
        computed:{
            dashOffset(){
                return(1-this.percent) * this.dashArray
            }
        }
    }
</script>

<style scoped>
    svg{
        position: relative;
    }
    circle {
        stroke-width: 10px;
        transform-origin: center;
        transform-origin: center;
        transform:scale(0.9);
    }

    .progress-background{
        stroke: rgb(238, 238, 238);
        transform:scale(0.9);
    }
    .progress-bar{
        stroke:rgba(114, 188, 213,1);
        transform: rotate(-90deg) scale(0.9);
    }
</style>