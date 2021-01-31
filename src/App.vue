<template>
  <div id="app">
    <Calculator />
  </div>
</template>

<script>
import Calculator from "./main/Calculator";

export default {
  components: { Calculator },
};
</script>

<style>
* {
  font-family: monospace;
}

body {
  margin: 0;
}

#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;

  height: 100vh;

  background: linear-gradient(to right, rgb(83, 105, 118), rgb(41, 46, 73));
}
</style>