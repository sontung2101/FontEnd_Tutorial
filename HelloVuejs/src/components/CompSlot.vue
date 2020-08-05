<template>
    <div class="comp-slot">
        <h1>Demo Slot</h1>
        <slot></slot>
        <h2>-----------------------</h2>
    </div>
  
</template>

<script>
export default {
    name:'comp-slot',
    data(){
        return{

        }
    },
    methods:{
        
    }

}
</script>

<style>
    .comp-slot{
        margin-top: 50px;
        padding: 100px 30px;
        border: 1px solid #000;
        margin-bottom: 50px;
    }
</style>