<template>
  <div id="app">
    <div v-if="!isAuthenticated">
      <h1>Witaj w systemie do zapisów na zajęcia</h1>
      <p>Zaloguj się e-mailem <input type="email" v-model="email">
      <button @click="logIn()">Wchodzę</button></p>
    </div>
   <div v-else>
    <h2>Zalogowany jako {{email }}</h2>
    <button @click="logOut()">Wyloguj</button>
   </div>


  </div>
  
  
  
</template>

<script>
import "milligram";
export default {
  name: 'app',
  data () {
    return {
      email: '...',
      isAuthenticated: false
    }
  },
methods: {
  logIn() {
  this.isAuthenticated=true;
  },
  logOut() {
  this.isAuthenticated=false;
  }
}
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
