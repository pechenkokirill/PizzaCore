<template>
  <navbar/>
  <router-view/>
</template>

<script>
import Navbar from './components/Navbar.vue'


export default {
  components:
  { 
    Navbar,
  }
}
</script>

<style>

@font-face {
  font-family: 'Meter';
  src: url(../public/fonts/Maler.ttf);
}

.text-white
{
  color: white;
}

.container
{
    margin-left: auto;
    margin-right: auto;
    max-width: 1366px;
    padding-left: 32px;
    padding-right: 32px;
}

.btn
{
   border-radius: 5px;
   border: 0;
   padding: 8px 16px;
   cursor: pointer;
   transition: opacity 250ms;
}

.btn:hover
{
  opacity: 0.8;
}

a
{
   text-decoration: none;
}

body
{
   background-repeat: repeat;
   background-image: url(../public/img/back.jpg);
   background-size: 256px;
   margin: 0;
}

.flex
{
  display: flex;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
