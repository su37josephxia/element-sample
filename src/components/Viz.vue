<template>

    <div class="viz">
        <el-col :span="6">
            <el-row>
                图表类型
            </el-row>
            <el-row>
                <img src="../assets/dataimg.png">
                <img src="../assets/dataimg1.png">
                <img src="../assets/dataimg2.png">
            </el-row>

            <el-row>

                <img src="../assets/dataimg3.png">
                <img src="../assets/dataimg4.png">
            </el-row>


            <el-row>

                <span class="txt">Lable:</span>
                <el-select v-model="value" placeholder="请选择" size="mini">
                    <el-option
                            v-for="item in options"
                            :key="item.value"
                            :label="item.label"
                            :value="item.value">
                    </el-option>
                </el-select>
            </el-row>

            <el-row>
                    <span class="txt">Value:</span>
            </el-row>

        </el-col>

        <el-col :span="21">


        </el-col>
    </div>
</template>

<script>
    export default {
        name: 'viz',
        data () {
            return {
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
            console.log('created....', this.msg)
        },
        components: {}
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    img {
        width: 42px;
        height: 24px;
    }
    .txt {font-size: 15px}
</style>
