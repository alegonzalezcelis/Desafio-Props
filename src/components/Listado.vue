<template>
<div class="listado">
    <li class="mb-3">
        {{ tarea }}
    </li>
    <button @click="eliminarTarea" type="button" class="btn btn-outline-danger btn-sm mb-3">Eliminar</button>
    <br>
</div>
</template>

<script>
export default {
name: 'Listado',
props: {
    tarea: String,
    index: Number
},
methods: {
    eliminarTarea(){
        this.$emit("eliminarTarea", this.index)
    }
}
}
</script>

<style>
.listado {
    display: flex;
    justify-content: center;
}

.listado > li {
    width: 50%;
}

</style>