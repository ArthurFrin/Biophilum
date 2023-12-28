<script setup lang="ts"></script>
<template>
  <div class="header">
    <img src="../assets/img/header.png" alt="" />
  </div>
</template>
<style lang="scss" scoped>
.header {
  width: 100%;
  height: auto;
  display: flex;
  justify-content: center;
  align-items: center;

  img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
}
@media screen and (max-width: 1200px) {
  .header {
    height: auto;
  }
}
</style>
