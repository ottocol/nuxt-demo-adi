<template>
  <h1>{{ valor }}</h1>
  <button @click="increment">Incrementar</button>
</template>

<script>
export default {
  data: function () {
    return { valor: 0 };
  },
  methods: {
    increment() {
      this.valor++;
    },
  },
};
</script>
