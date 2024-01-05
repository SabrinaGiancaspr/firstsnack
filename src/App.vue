<template>
  <div class="container">
    <div class="snack " id="first">
      <Firstsnack />
    </div>
    <div class="snack" id="second">
      <Secondsnack/>
    </div>
    <div class="snack" id="third">
      <Thirdsnack/>
    </div>
    <div class="snack" id="fourth">
      <Fourthsnack/>
    </div>
    <div class="snack" id="fifth">
      <Fifthsnack/>
    </div>
  </div>

</template>

<script setup>
import Secondsnack from './components/secondsnack.vue';
import Firstsnack from './components/firstsnack.vue';
import Thirdsnack from './components/thirdsnack.vue';
import Fourthsnack from './components/fourthsnack.vue';
import Fifthsnack from './components/fifthsnack.vue';
</script>

<style lang="scss" scoped>
.container{
  max-width: 1200px; 
  margin-left: auto; 
  margin-right: auto;
  padding-left: 15px;
  padding-right: 15px;

  #first{
    background-color: rgba(187, 18, 18, 0.188);
  }

  #second{
    background-color: rgba(0, 0, 255, 0.205);
  }

  #third{
    background-color: rgba(128, 0, 128, 0.221);
  }

  #fourth{
    background-color: rgba(0, 255, 255, 0.178);
  }

  #fifth{
    background-color: rgba(255, 0, 0, 0.377);
  }
  .snack{
    padding: 10px;
    margin-bottom: 80px;
  }
}
</style>