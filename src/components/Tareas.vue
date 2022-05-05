<template>
  <div class="tareas container">
      <h1 class="text-center mt-4 text-secondary">To Do List</h1>
      <div class="inpout-group mt-3">
          <input v-model="tarea" type="text" class="form-control" placeholder="Ingresa una tarea">
          <button @click="addTarea" class="btn btn-outline-secondary" type="submit">Crear</button>
      </div>
      <Listado :tarea="tarea" :index="$index"/>
  </div>
</template>

<script>
import Listado from './Listado.vue'
export default {
name: 'Tareas',
components: { Listado },
data: () => ({
    tarea: '',
    tareas: []
}),
methods: {
    addTarea() {
        this.tareas.unshift(this.tarea)
        this.tarea=''
        alert('add funcionando')
    }
}
}
</script>

<style>

</style>