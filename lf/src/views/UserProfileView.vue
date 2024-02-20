<script setup>
import { useRoute } from 'vue-router';
import { ref } from 'vue';

import users from "@/assets/users.json"

const route = useRoute();
const id = ref(route.params.userId); 
const user = users[id.value]
</script>

<template>
    {{ user.firstname }} {{ user.lastname }} <br>
    {{ user.email }}
</template>