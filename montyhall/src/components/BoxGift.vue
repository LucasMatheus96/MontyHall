<template>
  
    <div class="BoxGift">
      <div class="BoxGift-tie-1"></div>
      <div class="BoxGift-tie-2"> </div>
      <div class="BoxGift-top"></div>
      <div class="BoxGift-body"></div>
    </div>
     

  

             
</template>

<script>
export default {
name:'BoxGift'
}
</script>

<style>

.BoxGift{
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  z-index: 10;
}

.BoxGift-top{
  width: 100px;
  height: 25px;
  background-color: #7aa944;

}
 .BoxGift-body{
  width: 90px;
  height: 60px;
  background-color: #5c7e32;
} 
.BoxGift-tie-1{
  position: absolute;
  width: 15px;
  height: 85px;
  background-color: red;
} 

.BoxGift-tie-2{
  position: absolute;
  top:40px;
  width: 90px;
  height: 15px;
  background-color: red;
} 
</style>