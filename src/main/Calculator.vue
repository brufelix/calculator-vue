<template>
  <div class="calculator">
    <Display :value="displayValue" />
    <Button label="AC" triple @onClick="clearMemory" />
    <Button label="/" operation @onClick="setOperation" />
    <Button label="7" @onClick="setDigit" />
    <Button label="8" @onClick="setDigit" />
    <Button label="9" @onClick="setDigit" />
    <Button label="*" operation @onClick="setOperation" />
    <Button label="4" @onClick="setDigit" />
    <Button label="5" @onClick="setDigit" />
    <Button label="6" @onClick="setDigit" />
    <Button label="-" operation @onClick="setOperation" />
    <Button label="1" @onClick="setDigit" />
    <Button label="2" @onClick="setDigit" />
    <Button label="3" @onClick="setDigit" />
    <Button label="+" operation @onClick="setOperation" />
    <Button label="0" double @onClick="setDigit" />
    <Button label="." @onClick="setDigit" />
    <Button label="=" operation />
  </div>
</template>

<script>
import Button from "../components/Button";
import Display from "../components/Display";

export default {
  components: { Button, Display },
  data() {
    return {
      displayValue: "0",
      clearMemory: false,
    };
  },
  methods: {
    clearMemory() {
      this.value = 0;
    },
    setOperation(op) {
      this.value = op;
    },
    setDigit(digit) {
      this.value = digit;
    },
  },
};
</script>

<style>
.calculator {
  height: 320px;
  width: 235px;
  border-radius: 5px;
  overflow: hidden;

  display: grid;
  grid-template-columns: repeat(4, 25%);
  grid-template-rows: 1fr 48px 48px 48px 48px 48px;
}
</style>