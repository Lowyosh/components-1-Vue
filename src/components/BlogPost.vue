<script setup>
// defineProps(['title', 'id', 'body']);
defineProps({
    title: String,
    id: Number,
    body: {
        type: String,
        default: 'Sin Descripción',
    }
})
const emit = defineEmits(['cambiarFavoritoNombre'])

</script>

<template>
    <div class="card">
        <div class="card-body">
            <h5 class="card-title">{{title}}</h5>
            <p>{{body}}</p>
            <button @click="emit('cambiarFavoritoNombre', title)" class="btn btn-outline-primary">Fav</button>
        </div>
    </div>
</template>



<style>

</style>