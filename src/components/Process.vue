<template>
    <div>
        <el-col :span="9">
            <div>
                <el-button type="text" icon="menu" @click="isPivot = !isPivot">Pivot Table</el-button>
            </div>

            <div>
                <el-button type="text" icon="setting">过滤行数据</el-button>
            </div>
            <div>
                <el-col :span="9">
                    <el-select v-model="value" placeholder="请选择" size="mini">
                        <el-option
                                v-for="item in options"
                                :key="item.value"
                                :label="item.label"
                                :value="item.value">
                        </el-option>
                    </el-select>
                </el-col>
                <el-col :span="6">
                    <el-select v-model="value" placeholder="请选择" size="mini">
                        <el-option
                                v-for="item in options"
                                :key="item.value"
                                :label="item.label"
                                :value="item.value">
                        </el-option>
                    </el-select>
                </el-col>
                <el-col :span="6">
                    <el-input placeholder="请输入" size="mini"></el-input>
                </el-col>
                <el-col :span="3">
                    <el-button type="primary" icon="minus" size="mini"></el-button>
                </el-col>
            </div>
            <div>
                <el-button type="primary" icon="plus" size="mini"></el-button>
            </div>
            <div>
                <el-button type="text" icon="setting">过滤列数据</el-button>
                <div>
                    <el-button size="small">全选</el-button>
                    <el-button size="small">全不选</el-button>
                </div>
                <div>
                    <el-checkbox >列1</el-checkbox>
                </div>
                <div>
                    <el-checkbox >列2</el-checkbox>
                </div>
                <div>
                    <el-checkbox >列3</el-checkbox>
                </div>
                <div>
                    <el-checkbox >列4</el-checkbox>
                </div>
                <div>
                    <el-checkbox >列5</el-checkbox>
                </div>
                <div>
                    <el-checkbox >列6</el-checkbox>
                </div>
                <div>
                    <el-checkbox >列7</el-checkbox>
                </div>
                <div>
                    <el-checkbox >列8</el-checkbox>
                </div>
            </div>
        </el-col>
        <el-col :span="15">
            <!--<transition name="el-fade-in">-->
            <div v-show="isPivot">
                Pivot table..........

            </div>
            <data-table v-show="!isPivot"></data-table>

            <!--</transition>-->
            <!--<transition name="el-fade-in">-->

            <!--</transition>-->
        </el-col>

    </div>
</template>

<script>

    import DataTable from './DataTable.vue'
    
    export default {
        name: 'process',
        data () {
            return {
                isPivot: false,
                options: [{
                    value: '选项1',
                    label: '黄金糕'
                }, {
                    value: '选项2',
                    label: '双皮奶'
                }, {
                    value: '选项3',
                    label: '蚵仔煎'
                }, {
                    value: '选项4',
                    label: '龙须面'
                }, {
                    value: '选项5',
                    label: '北京烤鸭'
                }],
                value: '',

            }
        },
        methods: {},
        created: function () {
            console.log('created....')
        },

        components: {DataTable}
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
