<script>
export default{
    data(){
        return{
            inputWord: '',
            convertedWord: ''
        };
    },
    methods:{
        converting(){
            let input = this.inputWord;
      let result = '';
      for (let i = 0; i < input.length; i++) {
        if (input[i] !== input[i + 1]) {
          result += input[i];
        }
      }
      this.convertedWord = result;
    }
  }
};
</script>

<template>
    <h1>Quarto snack</h1>
   <div>
    <input type="text" v-model="inputWord" placeholder="Inserisci la parola da convertire" />
    <button @click="converting()">Converti</button>

    <div v-if="convertedWord">
      <p>Parola inserita: {{ inputWord }}</p>
      <p>Parola convertita: {{ convertedWord }}</p>
    </div>
  </div>
</template>

<style>

</style>