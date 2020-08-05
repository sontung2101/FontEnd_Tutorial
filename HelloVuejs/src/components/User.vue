<template>
    <div class="user">
        <h3>{{user.email}} <button v-on:click="handleDelete">Delete</button></h3>
    </div>
  
</template>

<script>
export default {
    name:'user',
    props:{
        user:{
            type:Object,
            default:null,
        }
    },
    data(){
        return{

        }
    },
    methods:{
        handleDelete(e){
            var data = {
                id:this.user.id,
            };
            this.$emit('deleteUser',data);
            console.log('User.vue',e);
        }
    }

}
</script>

<style>
</style>