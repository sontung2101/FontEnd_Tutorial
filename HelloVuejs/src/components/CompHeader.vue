<template>
  <header>
      <h1>{{text}}</h1>
      <h2>{{title}}</h2>
      <button v-on:click="changeTitleHeader">Thay đổi title từ CompoHeader.vue</button>
      
  </header>
</template>

<script>
export default {
    name:'comp-header',
    props:{
        title:String,
    },
    data(){
        return {
            text:"Fabbi JSC",
            }
    },
    methods:{
        changeTitleHeader(e){
            var data = {
                title:"Data gửi thông qua biến event",
            }
            this.$emit('changeTitleEvent',data)

        }
    }

}
</script>

<style>

</style>