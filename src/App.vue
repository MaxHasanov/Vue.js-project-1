<template>
  <div id="app">
    <input type="number" v-model="operandOne">
    <input type="number" v-model="operandTwo">

    <p>Результат: {{result}}</p>

    <button @click="sum">+</button>
    <button @click="difference">-</button>
    <button @click="multiply">*</button>
    <button @click="division">/</button>
    <button @click="mathPow">**</button>
    <button @click="mathFloor">Int(/)</button>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      operandOne: 0,
      operandTwo: 0,
      result: 0,
    }
  },
  methods: {
    sum() {
      this.result = Number(this.operandOne) + Number(this.operandTwo);
    },
    difference() {
      this.result = Number(this.operandOne) - Number(this.operandTwo);
    },
    multiply() {
      this.result = Number(this.operandOne) * Number(this.operandTwo);
    },
    division() {
      this.result = Number(this.operandOne) / Number(this.operandTwo);
    },
    mathPow() {
      this.result = Math.pow(this.operandOne, this.operandTwo);
    },
    mathFloor() {
      this.result = parseInt(this.operandOne / this.operandTwo);
    }
  }
}
</script>

<style lang="scss">

</style>
