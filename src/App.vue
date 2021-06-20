<template>
<archi-card>
  Salut !
</archi-card>


</template>

<script lang="ts">
import { defineComponent } from 'vue'
import ArchiCard from './components/ArchiCard.vue'


export default defineComponent({
  name: 'App',
  components: {
    ArchiCard
  }
})
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Public+Sans:ital,wght@0,200;0,400;0,600;0,700;1,200;1,400&display=swap');
#app {
  background-color:#2b2b2b;
  position: absolute;
  top:0;
  bottom:0;
  left:0;
  right:0;
  display: flex;
  justify-content: center;
  font-family: 'Public Sans', sans-serif;
}
</style>
