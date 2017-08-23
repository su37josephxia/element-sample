<template>
    <div>

        <top></top>
        <!--<el-menu :default-active="activeIndex2" class="el-menu-demo" mode="horizontal" @select="handleSelect">-->
            <!--<el-menu-item index="1"></el-menu-item>-->
            <!--&lt;!&ndash;<el-submenu index="2">&ndash;&gt;-->
            <!--&lt;!&ndash;<template slot="title">我的工作台</template>&ndash;&gt;-->
            <!--&lt;!&ndash;<el-menu-item index="2-1">选项1</el-menu-item>&ndash;&gt;-->
            <!--&lt;!&ndash;<el-menu-item index="2-2">选项2</el-menu-item>&ndash;&gt;-->
            <!--&lt;!&ndash;<el-menu-item index="2-3">选项3</el-menu-item>&ndash;&gt;-->
            <!--&lt;!&ndash;</el-submenu>&ndash;&gt;-->
            <!--&lt;!&ndash;<el-menu-item index="3"><a href="https://www.ele.me" target="_blank">订单管理</a></el-menu-item>&ndash;&gt;-->
        <!--</el-menu>-->



        <el-tabs v-model="activeName" @tab-click="handleClick">

            <el-tab-pane label="选择数据" name="1">
                <selector></selector>
            </el-tab-pane>
            <el-tab-pane label="处理数据" name="2">
                <process></process>
            </el-tab-pane>
            <el-tab-pane label="数据可视化" name="3">
                <viz></viz>
            </el-tab-pane>

            <el-tab-pane label="分享" name="4">
                <share></share>
            </el-tab-pane>
        </el-tabs>
        <div class="save">
            <el-button type="primary" icon="arrow-left">上一步</el-button>
            <el-button type="primary">下一步<i class="el-icon-arrow-right el-icon--right"></i></el-button>

        </div>

        <!---->
        <!--&lt;!&ndash;<input type="submit" value="确认添加"  class="btn btn-primary"/>&ndash;&gt;-->

    </div>

</template>

<style>

    #app {
        font-family: Helvetica, sans-serif;
        text-align: center;
        background-color: #f3f3f4;

    }

    .save {
        position: fixed;
        bottom: 100px;
        right:100px;
    }
</style>

<script>
    import Top from './components/top.vue'
    import Selector from './components/selector.vue'
    import Process from './components/process.vue'
    import Viz from './components/viz.vue'
    import Share from './components/share.vue'

    export default {
        data () {
            return {
                activeName: '1'
            }
        },

        methods: {
            handleClick(tab, event) {
                console.log(tab, event);
            }
        },
        components: {
            Top, Selector, Process, Viz, Share
        }

    }
</script>


