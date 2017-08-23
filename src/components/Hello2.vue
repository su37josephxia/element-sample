<template>
  <div class="hello2">

    <el-button icon="search" id='bt' @click.native="startHacking">Home2</el-button>



  </div>
</template>

<script>
export default {
  name: 'hello2',
  data () {
    return {

    }
  },
  methods: {

  },
  created: function () {
    console.log('created....',this.msg)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
