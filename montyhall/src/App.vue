<template>
  <div id="app">
    <h1>Problema de Monty Hall</h1>
    <div class="form">
      <div v-if="!started">
        <label for="portsAmount">Quantidade de Portas: </label>
        <input 
              type="text" 
              id="portsAmount" 
              size ="3"
              v-model.number="portsAmount"
        >
      </div>
      <div v-if="!started">
        <label for="selectedPort">Qual a porta é premiada ?</label>
        <input type="text" id="selectedPort" size="3" v-model.number="selectedPort">
      </div>
    </div>
    <button v-if="!started" @click="started= true">Iniciar</button>      
    <button v-if="started" @click="started= false">Reiniciar</button>      
  
    <div class="doors" v-if="started">
      <div vfor="i in portsAmount" :key="i">
        <DoorDisplay :hasGift="i== selectedPort"  :number="i"></DoorDisplay>
      </div>
    </div>

  </div>
</template>

<script>
import DoorDisplay from './components/DoorDisplay.vue'
  


export default {
  name:'App',
  components:{DoorDisplay},
  data: function (){
    return{
      started:false,
      portsAmount:3,
      selectedPort: null
    }
  }
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