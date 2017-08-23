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
                    <el-input v-model="input" placeholder="请输入" size="mini"></el-input>
                </el-col>
                <el-col :span="3">
                    <el-button type="primary" icon="delete" size="mini"></el-button>
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
                    <el-checkbox v-model="checked">列1</el-checkbox>
                </div>
                <div>
                    <el-checkbox v-model="checked">列2</el-checkbox>
                </div>
                <div>
                    <el-checkbox v-model="checked">列3</el-checkbox>
                </div>
                <div>
                    <el-checkbox v-model="checked">列4</el-checkbox>
                </div>
                <div>
                    <el-checkbox v-model="checked">列5</el-checkbox>
                </div>
                <div>
                    <el-checkbox v-model="checked">列6</el-checkbox>
                </div>
                <div>
                    <el-checkbox v-model="checked">列7</el-checkbox>
                </div>
                <div>
                    <el-checkbox v-model="checked">列8</el-checkbox>
                </div>
            </div>
        </el-col>
        <el-col :span="15">
            <!--<transition name="el-fade-in">-->
            <div v-show="isPivot">
                Pivot table..........

            </div>
            <!--</transition>-->
            <!--<transition name="el-fade-in">-->
            <el-table v-show="!isPivot"
                      :data="tableData3"
                      height="250"
                      border
                      style="width: 100%">
                <el-table-column
                        prop="date"
                        label="日期"
                        width="180">
                </el-table-column>
                <el-table-column
                        prop="name"
                        label="姓名"
                        width="180">
                </el-table-column>
                <el-table-column
                        prop="address"
                        label="地址">
                </el-table-column>
            </el-table>
            <!--</transition>-->
        </el-col>

    </div>
</template>

<script>
    export default {
        name: 'process',
        data () {
            return {
                isPivot: false,

                tableData3: [{
                    date: '2016-05-03',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1518 弄'
                }, {
                    date: '2016-05-02',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1518 弄'
                }, {
                    date: '2016-05-04',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1518 弄'
                }, {
                    date: '2016-05-01',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1518 弄'
                }, {
                    date: '2016-05-08',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1518 弄'
                }, {
                    date: '2016-05-06',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1518 弄'
                }, {
                    date: '2016-05-07',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1518 弄'
                }]

            }
        },
        methods: {},
        created: function () {
            console.log('created....')
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
