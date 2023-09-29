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

<style>
.container {
  margin: 0 auto;
  text-align: center;

  display: flex;
  flex-direction: column;
  gap: 3em;

  max-width: 600px;
  width: 600px;
}
</style>
