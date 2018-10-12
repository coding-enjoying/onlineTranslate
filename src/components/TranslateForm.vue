<template>
  <div class="translate-form">
    <form v-on:submit.prevent="onSubmit">
      <input type="text" value="请输入翻译的内容" v-model="input">
      <select>
        <option value="en">English</option>
      </select>
      <input type="submit" value="翻译"/>
    </form>
  </div>
</template>

<script>
export default {
  name: 'translate-form',
  data () {
    return {
      input:""
    }
  },
  methods:{
    onSubmit:function(){
      // console.log('lll');
      this.$emit("getInput",this.input);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
