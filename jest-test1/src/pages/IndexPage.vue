<template>
  <div class="htmlClass">
    <h1>{{ title }}</h1>
    <form>
      <input type="text" id="firstValue" v-model="firstValue" />
      <input type="text" id="secondValue" v-model="secondValue" />
      <input type="text" id="answerVulue" v-model="answerVulue" />
      <button @click="addition(firstValue,secondValue)" >Addition</button>
      <button @click="subtraction(firstValue,secondValue)" >Subtraction</button>
      <button @click="multiplication(firstValue,secondValue)" >Multiplication</button>
      <button @click="divide(firstValue,secondValue)" >Divide</button>
      <input type="text" id="firstName" v-model="firstName" />
      <input type="text" id="lastName" v-model="lastName" />
      <input type="text" id="id" v-model="id" />
  </form>
  </div>
</template>
<script>

export default {
  name: 'HtmlComponent',
  data() {
    return {
      title: 'Vue is awesome.',
      firstValue:0,
      secondValue:0,
      answerVulue:0,
      firstName:"Peeraphat",
      lastName:"Bangkan",
      id:"6404101329"
    }
  },
  methods: {
    // https://jestjs.io/docs/using-matchers
    // https://www.philbarresi.com/jest-test-guide/
    addition(first, second) {
      this.answerVulue =  Number(first) + Number(second)
      return this.answerVulue;
    },
    subtraction(first, second ) {
      this.answerVulue =  Number(first) - Number(second)
      return this.answerVulue;
    },
    multiplication(first, second ) {
      this.answerVulue =  Number(first) * Number(second)
      return this.answerVulue;
    },
    divide(first, second) {
      this.answerVulue =  Number(first) / Number(second)
      return this.answerVulue;
    },
  },
}
</script>
