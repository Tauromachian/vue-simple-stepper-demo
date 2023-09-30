<template>
  <div class="container">
    <h1>Vue Simple Stepper</h1>

    <div class="links-container">
      <a href="https://github.com/Tauromachian/vue-simple-stepper">
        <icon-helper icon="mdiGithub" width="50px" height="50px" />
      </a>
      <a href="https://www.npmjs.com/package/vue-simple-stepper">
        <icon-helper icon="mdiNpm" width="50px" height="50px" />
      </a>
    </div>
    <app-card>
      <card-text>
        <example-one></example-one>
      </card-text>
    </app-card>
  </div>
</template>

<script setup>
import "prismjs/themes/prism-okaidia.min.css";
import "prismjs";
</script>

<style>
.container {
  margin: 0 auto;

  display: flex;
  flex-direction: column;

  max-width: 600px;
  width: 600px;
}

.links-container {
  display: flex;
  gap: 1em;
  justify-content: center;
}
</style>
