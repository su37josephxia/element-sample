<template>

    <div class="share">
        <el-col :span="12">
            <el-row>
                保存格式
            </el-row>
            <el-row>
                <span class="txt">访问链接</span>
                <el-input size="mini" v-model="url"></el-input>
            </el-row>
            <el-row>
                <span class="txt">保存格式</span>
                <el-select v-model="value" placeholder="请选择" size="mini">
                    <el-option
                            v-for="item in options"
                            :key="item.value"
                            :label="item.label"
                            :value="item.value">
                    </el-option>
                </el-select>
                <el-button >保存</el-button>
            </el-row>

            <el-row>
                <div class="txt">iFrame embed</div>
                <el-input
                        type="textarea"
                        :autosize="{ minRows: 2, maxRows: 4}"
                        placeholder="请输入内容"
                        v-model="iframe">
                </el-input>
            </el-row>
        </el-col>
        <el-col :span="12">

        </el-col>
    </div>
</template>

<script>
    export default {
        name: 'share',
        data () {
            return {
                url:'http://hanabi.polomi.com/tableviz/share.html',
                iframe:'aaaaaaaaaaaa',
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
    .txt {font-size: 15px}
</style>
