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
    <p>
      Stepper component designed to guide users through a multi-step process,
      like a registration form or setup process. It provides a clear indication
      of the current, completed, and upcoming steps, and also allows for
      navigating between these steps.
    </p>
    <features-section></features-section>
    <section>
      <h2>Installation</h2>
      <p>Install it from npm</p>
      <one-line-code-highlighter>
        npm install vue-simple-stepper
      </one-line-code-highlighter>
      <p>You need to import the component doing:</p>
      <one-line-code-highlighter>
        import VueSimpleStepper from 'vue-simple-stepper'
      </one-line-code-highlighter>
      <p>And its styles like this:</p>
      <one-line-code-highlighter>
        import "vue-simple-stepper/dist/style.css";
      </one-line-code-highlighter>
    </section>
    <div>
      <h2>Use</h2>
      <p>The easiest way to use is to copy and throw this in your code:</p>
    </div>
    <pre class="language-html" data-src="ExampleOne.vue"></pre>
    <p>
      Any element found in the default slot of the component will be
      automatically added to the stepper. Notice that the steps data prop number
      coincides with the number of elements in the stepper.
    </p>
    <p>
      You can set a default starting point of the component with the step prop.
      With it you can also control the stepper programmatically.
    </p>
    <p>Any time the actions of the stepper are clicked the events:</p>
    <ul>
      <li>click:next</li>
      <li>click:previous</li>
      <li>
        click:submit Are going to be emitted in by the stepper on click of the
        respective action.
      </li>
    </ul>
    <p>
      One common problem is the customization of the stepper to fit the
      framework or styles of choice. In that case you can do it by using the CSS
      variables:
    </p>
    <pre class="language-css" data-src="root-general-styles.css"></pre>
    <p>
      Or in case you want to further customize the buttons you can overwrite or
      extend these classes:
    </p>
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
