<template>
  <div class="container">
      <h1 class="text-center mt-4 text-secondary">To Do List</h1>
      <div class="input-group mt-3">
          <input v-model="tarea" type="text" class="form-control" placeholder="Ingresa una tarea">
          <button @click="addTarea" class="btn btn-outline-secondary">Crear</button>
      </div>
      <h2 class="text-center my-5 text-secondary">Lista</h2>
      <ol>
          <div class="lista">
              <Listado @eliminarTarea="eliminarTarea($event)" v-for="(tarea, $index) in tareas" :key="$index" :tarea="tarea" :index="$index"/>
          </div>
      </ol>
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
    },
    eliminarTarea() {
        this.tareas.splice(key,1)
    }
}
}
</script>

<style>
.lista {
  display: flex;
  justify-content: center;
}

.listado > li {
  width: 100%;
}
</style>