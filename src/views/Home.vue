<template>
    <div class="topnavAndBanner">
        <Topnav/>
        <div class="banner">
            <h1>路鹿 UI</h1>
            <h2>一个简单的 UI 框架</h2>
            <p class="actions">
                <a href="https://github.com/baozi928">GitHub</a>
                <router-link to="/doc">开始</router-link>
            </p>
        </div>
    </div>
</template>

<script lang="ts">
    import Topnav from '../components/Topnav.vue'
    export default {
        components: {Topnav}
    }
</script>

<style lang="scss" scoped>
    .topnavAndBanner {
        background: linear-gradient(145deg, rgba(195,241,236,1) 0%, rgba(253,221,252,1) 100%);
        clip-path: ellipse(70% 60% at 50% 40%);

    }
    .banner {
        padding: 100px 0;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        > .actions{
            padding: 8px 0;
            a {
                margin:0 8px;
                background: #fff;
                display: inline-block;
                $h: 28px;
                height: $h;
                line-height: $h;
                border-radius: $h/2;
                padding: 0 8px;
            }
        }
    }

</style>