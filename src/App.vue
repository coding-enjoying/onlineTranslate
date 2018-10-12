<template>
  <div id="app">
    <h1>在线翻译</h1>
    <h5>简单 / 易用 / 便捷</h5>
    <TranslateForm v-on:getInput="translate($event)"></TranslateForm>
    <TranslateOutput v-text="translatedText"></TranslateOutput>
  </div>
</template>

<script>
import TranslateForm from './components/TranslateForm'
import TranslateOutput from './components/TranslateOutput'

export default {
  name: 'App',
  components: {
    TranslateForm,TranslateOutput
  },
  data(){
    return{
      translatedText:""
    }
  },
  methods:{
    translate:function(content){
      // console.log(content);
      // this.$http.get('https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20180803T135529Z.ac4296ea5211e0f0.2efb9ebd65c3b82e149ebd95f29f2f0ba33e0c98&lang='+language+'&text='+content).then((res)=>{
      //   // console.log(res);
      //   this.translatedText = res.body.text[0];
      // })
      this.$http.get('https://translate.yandex.net/api/v1.5/tr.json/translate?key=trnsl.1.1.20180803T135529Z.ac4296ea5211e0f0.2efb9ebd65c3b82e149ebd95f29f2f0ba33e0c98&lang=en&text='+content).then((res)=>{
        // console.log(res);
        this.translatedText = res.body.text[0];
      })
    }
  }
}
</script>

<style>

</style>
