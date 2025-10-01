<template>
  <div id="app">
    <BaseCard></BaseCard>
  </div>
  
</template>

<script>
import BaseCard from './components/BaseCard.vue';


export default {
  name: 'App',
  components: {BaseCard
  }
}
</script>

<style>

html{
}
body{
  margin: 0;
  background: radial-gradient(71.11% 100% at 50% 0%, #020204 14.6%, #011F35 100%);
  box-sizing: border-box;


}

#app{
  min-height: 100vh;
  width: 100vw;
}

</style>
