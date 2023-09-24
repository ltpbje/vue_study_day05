<template>
  <div>
    <MyDialog>
      <template v-slot:head>
        我是头部
      </template>
      <template v-slot:content>
        我是内容
      </template>
      <template #foot>
        <button>确定</button>
        <button>取消</button>
      </template>
    </MyDialog>
  </div>
</template>

<script>
import MyDialog from './components/MyDialog'
export default {
  data () {
    return {

    }
  },
  components: {
    MyDialog
  }
}
</script>

<style>
body {
  background-color: #b3b3b3;
}
</style>