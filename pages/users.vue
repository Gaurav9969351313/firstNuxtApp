<template>
      <div>
        <input type="text" v-model="userId">
        <button @click="onLoadUser">Load Users</button>
        please enter id and redirect
        <nuxt-child />
      </div>
</template>

<script>
    export default {
        data() {
        return {
            'userId':"Gaurav Talele"
        }
        },
        methods:{
            onLoadUser(){
            this.$router.push("/users/"+this.userId);
            }
        }
    }
</script>

