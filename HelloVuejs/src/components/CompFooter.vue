<template>
  <footer>
      <h1>{{text}}</h1>
      <h1>{{title}}</h1>
    </footer>
</template>

<script>
export default {
    name:'comp-footer',
    props:{
        title:String,
    },
    data(){
        return{
            text:"Footer-HiImST",
        }
    }

}
</script>

<style>

</style>