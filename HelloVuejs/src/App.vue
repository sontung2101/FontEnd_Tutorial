<template>
  <div id="app">
    <comp-header 
    v-bind:title="title"
    v-on:changeTitleEvent="handleChangeTitle"
    />
    <img src="./assets/logo.png">
    <h1>{{ msg }}</h1>
    <list-user v-bind:listUser="listUser" v-on:deleteUserEvent="deleteUserEvent" />
    <comp-footer v-bind:title="title"/>
    <comp-slot>
      <div>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Culpa obcaecati ratione reprehenderit ab quod, autem voluptas minima, doloremque consequatur deleniti rerum magnam architecto tempore dolor neque omnis. Ipsam, dicta nostrum!</p>
      </div>
    </comp-slot>
    <demo-slot/>
  </div>
</template>

<script>
import CompHeader from './components/CompHeader.vue';
import CompFooter from './components/CompFooter.vue';
import ListUser from './components/ListUser.vue';
import CompSlot from './components/CompSlot.vue';
import DemoSlot from './components/DemoSlot.vue';
export default {
  name: 'app',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      title:"Title ở app",
      listUser:[
        {id:1,email:'sontung2101@mail.com',active:true},
        {id:2,email:'sontung2101+1@mail.com',active:false},
        {id:3,email:'sontung2101+2@mail.com',active:true},
        {id:4,email:'sontung2101+3@mail.com',active:true}, 
        {id:5,email:'sontung2101+4@mail.com',active:false},
        {id:6,email:'sontung2101+5@mail.com',active:true},
        {id:7,email:'fabbi@mail.com',active:true},
      ]
    }
  },
  components:{
    CompHeader,
    CompFooter,
    ListUser,
    CompSlot,
    DemoSlot,
  },
  methods:{
    handleChangeTitle(data){
      this.title = data.title

      console.log("HandlechangeTitle App.Vue",data);
    },
    deleteUserEvent(data){
      var indexDelete = -1;
      this.listUser.forEach((u,idx)=>{
        console.log(u.id,idx,data.id)
        if( u.id === data.id){
          indexDelete = idx
        }
      })
      if(indexDelete != -1){
        this.listUser.splice(indexDelete,1)
      }
      console.log("Đã chạy đến file App.vue")
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
