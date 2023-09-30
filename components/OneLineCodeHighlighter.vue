<template>
  <div class="code-display-box">
    <pre>
        
<code><slot></slot></code>
    </pre>
    <button @click="copyToClipboard">Copy to Clipboard</button>
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
  border-radius: 3px; /* Slight rounded corners */
  padding: 2px 2px; /* Small padding for better presentation */
  font-family: "Courier New", Courier, monospace; /* Monospaced font for code */
  font-size: 0.95em; /* Slightly smaller font-size */
}

pre {
  margin: 0;
  padding: 0;
}

button {
  display: block;
  position: absolute;
  padding: 5px 15px;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 14px;
  top: 5px;
  right: 5px;
}

button:hover {
  background-color: #0056b3;
}
</style>
