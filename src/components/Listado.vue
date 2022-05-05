<template>
    <div>
        <h2 class="text-center my-5 text-secondary">Lista</h2>
        <ol>
            <div v-for="(tarea, $index) in tareas" :key="$index" class="lista">
                <li class="mb-3">{{ tarea }}holi</li>
                <button @click="tareas.splice(index, 1)" type="button" class="btn btn-outline-danger btn-sm mb-3">Eliminar</button>
            </div>
        </ol>
    </div>
</template>

<script>
export default {
name: 'Listado',
props: {
    tarea: String,
    index: Number
},
data: () => ({
    
})
}
</script>

<style>
.lista {
  display: flex;
  justify-content: center;
}
.lista > li {
  width: 50%;
}
</style>