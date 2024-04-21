<template>
  <div class="card mb-3">
    <img :src="iconUrl" class="card-img-top" alt="Chuck Norris">
    <div class="card-body">
      <p class="card-text">{{ value }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ChuckCard',
  props: ['iconUrl', 'value']
}
</script>

<style scoped>
.card {
  /* Agrega sombra y bordes redondeados a la tarjeta */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  border-radius: 0.25rem;
}

.card-img-top {
  height: 200px; /* o cualquier altura que prefieras */
  object-fit: cover; /* Asegura que la imagen cubra todo el espacio disponible */
  border-top-left-radius: calc(0.25rem - 1px);
  border-top-right-radius: calc(0.25rem - 1px);
}

.card-body {
  padding: 1rem;
}

.card-text {
  margin: 0;
}
</style>
