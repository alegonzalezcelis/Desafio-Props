<template>
  <div id="app">
    <Tareas />
  </div>
</template>

<script>
import Tareas from '@/components/Tareas.vue'

export default {
  name: 'app',
  components: {
    Tareas, 
  },
  data: () => ({
    tarea: '',
    tareas: '',
  })
}
</script>

<style>
#app {
    font-size: 38px;
    font-family: 'Calibri', sans-serif;
    color: darkblue;
}
img {
  width: 25%;
  height: 25%;
}
</style>
