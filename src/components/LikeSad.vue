Phadungkiat Sutayo
<script setup>
import { ref } from "vue";
const like = ref(0);
const sad = ref(0);

function likeClick() {
  like.value++;
}
function sadClick() {
  sad.value++;
}
</script>

<template>
  <center>
    <div class="col">
      <div class="card shadow-sm">
        <svg
          class="bd-placeholder-img card-img-top"
          width="450"
          height="225"
          xmlns="http://www.w3.org/2000/svg"
          role="img"
          aria-label="Placeholder: Thumbnail"
          preserveAspectRatio="xMidYMid slice"
          focusable="false"
        >
          <title>Placeholder</title>
          <rect width="100%" height="100%" fill="#CCFFFF"></rect>
          <text x="50%" y="50%" fill="#eceeef" dy=".3em">Thumbnail</text>
        </svg>
        <div class="card-body">
          <p class="card-text">
            This is a wider card with supporting text below as natural lead-in to
            additional content. This content is a little bit longer.
          </p>
          <div class="d-flex justify-content-between align-items-center">
            <div class="btn-group"></div>
          </div>
        </div>
      </div>
    </div>
    <div>
      <button @click="likeClick()">ปุ่ม like{{ like }}</button>

      <button @click="sadClick()">ปุ่ม sad {{ sad }}</button>
    </div>
  </center>
</template>

<style scoped></style>
