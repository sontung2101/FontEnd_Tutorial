<template>
    <div class="comp-tabs">
        <div class="tabs-title">
            <span>{{title}}</span>
            <!-- <ion-icon name="bus-outline"></ion-icon> -->
            <span>icon</span>
        </div>
         <div class="tabs-content">
            <slot></slot>
        </div>
    </div>
  
</template>

<script>
export default {
    name:'comp-tabs',
    data(){
        return{

        }
    },
    props:{
        title:String,
    }
 
}
</script>

<style>
    .tabs-title{
        border: 1px solid #000;
        display: flex;
        justify-content: space-between;
        padding:15px 30px
    }
    .tabs-content {
        border: 2px solid blue;
        margin-top: 2px;
        padding: 2px;
    }
    .tabs-hedear{
        list-style-type: None;
        margin:0;
        padding:0;
        display: flex;
    }
    .tabs-hedear li{
        width: 100%;
        padding:10px 20px;
        background-color: tomato;
        transition: all .3s ease;
        margin-bottom: 5px;
    }
    .tabs-hedear li:hover{
        color: white;
        background: #000;
    }
    .tab-content{
        padding: 15px;
        text-align: left;
        border: 2px solid teal;
    }
    .active{
        color: white;
    }

</style>