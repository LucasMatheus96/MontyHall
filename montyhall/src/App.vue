<template>
  <div id="app">
    <h1>Problema de Monty Hall</h1>
    <DoorDisplay number="1" :hasGift="false"></DoorDisplay>
  </div>
</template>

<script>
import DoorDisplay from './components/DoorDisplay.vue'
  


export default {
  name:'App',
  components:{DoorDisplay}
}
</script>

<style>
*{
  box-sizing: border-box;
  font-family: 'Montserrat',sans-serif;
}

body{
  color:#fff;
  background:linear-gradient(to right, rgb(21,153,87),rgb(21,87,153) )
}

#app{
  display: flex;
  flex-direction: column;
  align-items: center;
}

#app h1 {
  border: 1px solid #000;
  background-color: #0004;
  padding:20px;
  margin-bottom: 60px;
}
</style>