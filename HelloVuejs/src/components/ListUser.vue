<template>
  <div class="list-user">
        <h2>List Users Components</h2>
        <user v-for="user in listUser" v-bind:key="user.id" v-bind:user="user" v-on:deleteUser="deleteUser" />
  </div>
</template>

<script>
import User from './User.vue'
export default {
    name:'list-user',
    props:{
        listUser:{
            type:Array,
            default:[],
        },
    },
    data(){
        return{
            
        };
    },
    components:{
        User,
    },
    methods:{
        deleteUser(data){
            console.log('DeleteUser trong listUser.vue',data)
            this.$emit('deleteUserEvent',data)
        }
    }

}
/*
App
    Listuser -> ko được quyền thay đổi arrlistUser -> truyền trực tiếp Event thêm một lần nữa ra App.vue
        user -> truyền event thông báo ra cho listuser
        user
        user
*/ 

</script>

<style>

</style>