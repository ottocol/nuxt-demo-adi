<template>
  <div>
    <h1>Lista de personajes</h1>
    <ul>
      <li v-for="p in lista" :key="p.url">
        {{ p.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default defineNuxtComponent({
  fetchKey: 'personajes',
  async asyncData() {
    var datos = await $fetch('https://swapi.dev/api/people');
    return {
      lista: datos.results,
    };
  },
});
</script>
