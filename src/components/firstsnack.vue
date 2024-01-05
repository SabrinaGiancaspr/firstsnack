<script>
export default{
    data(){
        return{
            numbers: [],
            sum: 0,
            arrayLength: 0,
            output: 0,
        }
    },
    methods:{
        generateArray(){
            
            for(let i = 0; i < this.arrayLength; i++){
                const ranNum = Math.floor(Math.random() * 100)
                this.numbers.push(ranNum)
            }
        },
        arrayOutput(){
            for(let i = 0; i < this.numbers.length; i++){
                this.sum += this.numbers[i];
            }
            this.output = this.sum / 2;
        },

        refresh(){
            this.numbers = [];
            this.arrayLength = 0;
            this.output = 0;
            this.sum = 0;
        },

        newNumbers(){
            this.numbers = [];
            this.generateArray()
        }
    }
}
</script>

<template>
<button @click="refresh()" v-show="numbers.length > 0">refresh</button>
<label for="length">array length</label>
<input :readonly="numbers.length > 0" @keyup.enter="generateArray()" type="number" name="length" id="length" v-model="arrayLength">
<span v-for="number in numbers">{{ number }}, </span>
<button @click="newNumbers()" v-show="numbers.length > 0 && output == 0">new numbers</button>
<button v-show="numbers.length > 0 && output == 0" @click="arrayOutput()">output</button>
<span v-show="output > 0">output: {{ output }}</span>
</template>

<style>

</style>