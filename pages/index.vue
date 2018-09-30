<template>
  <section class="container">
    <div>
      <h1 class="title">
        firstNuxtApp
      </h1>
      <h4> <a href="/users">users</a> </h4>
      <h4><nuxt-link to="/users"> users with nuxt link </nuxt-link></h4>

      <div>
        <input type="text" v-model="userId">
        <button @click="onLoadUser">Load Users</button>
      </div>
    </div>
  </section>
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


<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
