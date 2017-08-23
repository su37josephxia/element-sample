<template>

    <div class="selector">
        <el-col :span="3">
            <div>
                <el-button type="text" icon="edit" @click="show = !show">选择数据</el-button>
            </div>
            <div>
                <el-button type="text" icon="upload2">上传文件</el-button>
            </div>
            <div>
                <el-button type="text" icon="search">粘贴数据</el-button>
            </div>
            <div>
                <el-button type="text" icon="share">来自URL</el-button>
            </div>
        </el-col>

        <el-col :span="21">
            <transition name="el-fade-in">
                <el-tree v-show="show" :data="data" :props="defaultProps" @node-click="handleNodeClick"></el-tree>
            </transition>
        </el-col>

    </div>
</template>

<script>
    export default {
        name: 'selector',
        data() {
            return {
                show: true,
                data: [{
                    label: '一级 1',
                    children: [{
                        label: '二级 1-1',
                        children: [{
                            label: '三级 1-1-1'
                        }]
                    }]
                }, {
                    label: '一级 2',
                    children: [{
                        label: '二级 2-1',
                        children: [{
                            label: '三级 2-1-1'
                        }]
                    }, {
                        label: '二级 2-2',
                        children: [{
                            label: '三级 2-2-1'
                        }]
                    }]
                }, {
                    label: '一级 3',
                    children: [{
                        label: '二级 3-1',
                        children: [{
                            label: '三级 3-1-1'
                        }]
                    }, {
                        label: '二级 3-2',
                        children: [{
                            label: '三级 3-2-1'
                        }]
                    }]
                }],
                defaultProps: {
                    children: 'children',
                    label: 'label'
                }
            };
        },
        methods: {
            handleNodeClick(data) {
                console.log(data);
            }
        },
        created: function () {
            console.log('created....', this.msg)
        },
        components: {}
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
