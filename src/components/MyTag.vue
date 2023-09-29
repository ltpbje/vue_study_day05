<template>
<div class="my-tag">
    <input v-if="isEdit"
    :value="value"
    v-focus
    @keyup.enter="handleEnter"
    class="input"
    type="text"
    placeholder="输入标签"
    @blur="isEdit = false "/>
    <div v-else 
    class="text" 
     @dblclick="showEdit">
      {{value}}
    </div>
</div>
</template>

<script>
export default {
  props:{
    value:String
  },
data(){
  return{ 
    isEdit:false
  }
},
methods:{
   showEdit(){
    this.isEdit = true
    // this.$nextTick(()=>{
    //   this.$refs.edit.focus();
    // })
   } ,
   handleEnter(e){
    // console.log('回车了');
    if(e.target.value.trim() === '') return alert('输入不能为空')
    this.$emit('input',e.target.value)
    this.isEdit = false
   }
}
}
</script>

<style lang="less" scoped>
  .my-tag {
    cursor: pointer;
    .input {
      appearance: none;
      outline: none;
      border: 1px solid #ccc;
      width: 100px;
      height: 40px;
      box-sizing: border-box;
      padding: 10px;
      color: #666;
      &::placeholder {
        color: #666;
      }
    }
  }
</style>