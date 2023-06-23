<script setup>
import BlogPost from './components/BlogPost.vue';
import ButtonCounter from './components/ButtonCounter.vue';
import { ref } from 'vue';


const posts = ref([
  {title: 'Post 1', id: 1, body: 'Descripción 1'},
  {title: 'Post 2', id: 2, body: 'Descripción 2'},
  {title: 'Post 3', id: 3 },
]);

const favorito = ref('')
const cambiarFavorito = (title) => {
  favorito.value = title;
}

</script>



<template>
  <div class="container">
    <h1>App</h1>
    <h2>Mis post favorito: {{ favorito }} </h2>
  </div>
  <BlogPost
  v-for="post in posts"
  :key="post.id"
  :title="post.title"
  :id="post.id"
  :body="post.body"
  @cambiarFavoritoNombre = 'cambiarFavorito'
  />

</template>


<style>

</style>