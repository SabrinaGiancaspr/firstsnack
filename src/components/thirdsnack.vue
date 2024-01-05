<script>
export default{
    data(){
        return{
            word1: '',
            word2:'',
            commonLetter: '',
        }
    },
    methods:{
        findCommonLetter(){
            let minLength = Math.min(this.word1.length, this.word2.length);
            for( let i = 0; i < minLength; i++){
                if(this.word1[i] === this.word2[i]){
                    this.commonLetter = this.word1[i];
                    return
                }
            }
            this.commonLetter = '';
        }
    }
}
</script>

<template>
    <h1>Terzo snack</h1>
  <div>
    <input v-model="word1" placeholder="Prima parola">
    <input v-model="word2" placeholder="Seconda parola">
    <button @click="findCommonLetter">Trova lettera comune</button>
    <p v-if="commonLetter !== ''">
      La lettera comune nella stessa posizione è: {{ commonLetter }}
    </p>
    <p v-else>
      Non ci sono lettere comuni nella stessa posizione.
    </p>
  </div>

</template>

<style>

</style>