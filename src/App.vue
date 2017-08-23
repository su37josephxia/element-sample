<template>

    <el-tabs v-model="activeName" @tab-click="handleClick">

        <el-tab-pane label="选择数据" name="selector">
                <selector></selector>
        </el-tab-pane>
        <el-tab-pane label="处理数据" name="process">
            <process></process>
        </el-tab-pane>
        <el-tab-pane label="数据可视化" name="viz">
            <viz></viz>
        </el-tab-pane>

        <el-tab-pane label="分享" name="share">
            <share></share>
        </el-tab-pane>
    </el-tabs>

</template>

<style>

    #app {
        font-family: Helvetica, sans-serif;
        text-align: center;

    }
</style>

<script>
    import Selector from './components/selector.vue'
    import Process from './components/process.vue'
    import Viz from './components/viz.vue'
    import Share from './components/share.vue'

    export default {
        data () {
            return {
                activeName: 'selector'
            }
        },

        methods: {
            handleClick(tab, event) {
                console.log(tab, event);
            }
        },
        components: {
            Selector, Process, Viz, Share
        }

    }
</script>


