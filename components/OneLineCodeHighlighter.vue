<template>
  <div class="code-display-box">
    <pre>
        
<code><slot></slot></code>
    </pre>
    <button @click="copyToClipboard">
      <icon-helper icon="mdiContentCopy"> </icon-helper>
    </button>
  </div>
</template>

<script setup>
const copyToClipboard = () => {
  const el = document.createElement("textarea");
  el.value = this.codeContent;
  document.body.appendChild(el);
  el.select();
  document.execCommand("copy");
  document.body.removeChild(el);
};
</script>

<style scoped>
.code-display-box {
  position: relative;
  background-color: rgba(
    135,
    131,
    120,
    0.15
  ); /* A subtle background similar to Medium */
  border-radius: 8px; /* Slight rounded corners */
  padding: 2px 2px; /* Small padding for better presentation */
  font-family: Consolas, Monaco, "Andale Mono", "Ubuntu Mono", monospace; /* Monospaced font for code */
  font-size: 0.95em; /* Slightly smaller font-size */
}

pre {
  margin: 0;
  padding: 0;
}

button {
  display: block;
  position: absolute;
  padding: 5px 5px;
  color: white;
  border: none;
  border-radius: 5px;
  background-color: transparent;
  cursor: pointer;
  font-size: 14px;
  top: 5px;
  right: 5px;
}
</style>
