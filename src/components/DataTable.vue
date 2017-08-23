<template>
    <div class="table">
        <el-table
                  :data="tableData3"
                  height="500"
                  border
                  style="width: 100%">
            <el-table-column
                    prop="date"
                    label="日期">
            </el-table-column>
            <el-table-column
                    prop="name"
                    label="姓名">
            </el-table-column>
            <el-table-column
                    prop="address"
                    label="地址">
            </el-table-column>
        </el-table>
    </div>
</template>

<script>


    export default {
        name: 'table',
        data() {
            var tableData3 = []
            for (var i = 0; i < 100; i++) {
                tableData3.push({
                    date: '2016-05-03',
                    name: '王小虎',
                    address: '上海市普陀区金沙江路 1518 弄'
                })
            }
            return {
                tableData3: tableData3
            }
        },

    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
