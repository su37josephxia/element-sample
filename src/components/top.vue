<template>

    <div class="top">
        <el-menu theme="dark" class="el-menu-demo" mode="horizontal">
            <!--<img src="../assets/logo.png" style="width: 42px;margin-left: 20px;">-->
            <span style="color:whitesmoke;margin-left: 15px;">Hanabi</span>
            <!--<el-menu-item index="1"></el-menu-item>-->
            <!--<el-submenu index="2">-->
                <!--<template slot="title">我的工作台</template>-->
                <!--<el-menu-item index="2-1">选项1</el-menu-item>-->
                <!--<el-menu-item index="2-2">选项2</el-menu-item>-->
                <!--<el-menu-item index="2-3">选项3</el-menu-item>-->
            <!--</el-submenu>-->
            <!--<el-menu-item index="3"><a href="https://www.ele.me" target="_blank">订单管理</a></el-menu-item>-->

            <el-button type="text" icon="close" style="float:right;margin-right: 15px;" >退出</el-button>

        </el-menu>
        <div class="line"></div>
    </div>
</template>

<script>
    export default {
        name: 'top',
        data () {
            return {}
        },
        methods: {},
        created: function () {
            console.log('created....', this.msg)
        },
        components: {}
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

    /*.top {*/
        /*background-color: #1c8de0;*/
        /*margin-right: -15px;*/
        /*margin-left:-15px;*/
        /*margin-bottom:0;*/

    /*}*/

</style>
