
<script>
export default {
  data() {
    return {
      number: 0,
      word: '',
      outputWord: ''
    };
  },
  methods: {
    updateOutput() {
      if (this.number % 2 === 0) {
        this.outputWord = this.word;
      } else {
        this.outputWord = this.word.split("").reverse().join("");
      }
    }
  }
};
</script>

<template>
    <h1>Secondo Snack</h1>
  <div>
    <label for="numberInput">Inserisci un numero:</label>
    <input id="numberInput" type="number" v-model="number" />
    <label for="wordInput">Inserisci una parola:</label>
    <input id="wordInput" type="text" v-model="word" />
    <button @click="updateOutput">invert</button>
    <p v-show="outputWord !== ''">Output: {{ outputWord }}</p>
  </div>
</template>

<style>
</style>