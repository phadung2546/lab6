<script setup>
import LikeSad from "./components/LikeSad.vue";
import { ref } from "vue";

const stuid = ref("");
const stuName = ref("");
</script>

<template>

  <div v-for="n in 6" :key="n">{{  }}<LikeSad> </LikeSad></div>

</template>

