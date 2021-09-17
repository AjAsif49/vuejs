<template>
  <div id="app">
    <h1>{{ title }}</h1>
    <Navbar></Navbar>
    <AllFriends :friends="friends"></AllFriends>
    <OnlineFriends :friends="friends"></OnlineFriends>
  </div>
</template>

<script>

import Navbar from './components/Navbar.vue'
import OnlineFriends from './components/OnlineFriends.vue'
import AllFriends from './components/AllFriends.vue'

export default {
  name: 'App',
  data(){
    return{
    title: "Wow",
    friends:[
                    { name: 'A', online:true },
                    { name: 'B', online:false },
                    { name: 'C', online:true },
                    { name: 'D', online:true },
                    { name: 'E', online:false }
                ]
  }
  },
  components:{
    Navbar,
    OnlineFriends,
    AllFriends
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
