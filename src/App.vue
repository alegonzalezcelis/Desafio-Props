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

</style>
