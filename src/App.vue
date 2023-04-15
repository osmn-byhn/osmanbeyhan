<script setup>
  import { RouterLink, RouterView } from 'vue-router'
  import Navbar from './components/Navbar.vue';
  //USING FOR GITHUB PARTS IN ABOUT-ME PAGES
  /*
  const fetchOrganization = async () => {
    //https://api.github.com/user
    const result = await fetch('https://api.github.com/users/osmn-byhn/repos', {
      method: "GET",
      headers: {
        "Accept": "application/vnd.github.v3+json"
      }
    })
    const _data = await result.json()
    console.log("data", _data)
    
  }
  fetchOrganization()
  */
 
</script>

<template>
  <Navbar />
  <RouterView />
</template>

<style scoped lang="scss">

</style>
