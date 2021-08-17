<template>
  <NuxtLink class="card" :to="`/products/${card.id}`">
    <img
      :src="require(`@/assets/images/${card.image}`)"
      alt="fe"
      class="image"
    />
    <h3 class="header">{{ card.title }}</h3>
    <p class="snippet">
      {{ card.snippet }}
    </p>
  </NuxtLink>
</template>

<script>
export default {
  props: ["card"],
};
</script>


<style scoped>
.card {
  width: 31.5%;
  height: 25rem;
  border: none;
  overflow: hidden;
  padding: 0;
  cursor: pointer;
}
.image {
  height: 65%;
  border-radius: 0.5rem;
}
.header {
  font-size: 1.15rem;
  margin-top: 0.4rem;
  color: black;
}
.header:hover {
  color: black;
  text-decoration: none;
}

.snippet {
  color: grey;
}
</style>