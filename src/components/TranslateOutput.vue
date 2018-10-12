<template>
  <div class="translate-output">
  	<h2>{{translatedText}}</h2>
  </div>
</template>

<script>
export default {
  name: 'translate-output',
  // props:{
  // 	translatedText:{
  // 		type:String,
  // 		required: true
  // 	}
  // },
  props:[
  	"translatedText"
  ],
  data () {
    return {
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
