<template>
  <div id="app" class="controle">
    <Controle />
  </div>
</template>

<script>
import Controle from './components/Controle.vue';

export default {
  components: {
    Controle,
  },
};
</script>

<style>
#app {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: #121212;
}
</style>
