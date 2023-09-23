<template>
  <div>
    <MyDialog>1</MyDialog>

    <MyDialog></MyDialog>
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