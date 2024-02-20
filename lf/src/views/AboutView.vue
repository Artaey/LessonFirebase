<script setup>
import { useRoute, useRouter } from "vue-router";

const route = useRoute();
const router = useRouter();
const routes = router.getRoutes();

console.log(routes);
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
    <menu>
      <li v-for="r in routes" :key="r.path">
        <RouterLink :to="r.path">{{ r.meta.title }}</RouterLink>
      </li>
    </menu>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
