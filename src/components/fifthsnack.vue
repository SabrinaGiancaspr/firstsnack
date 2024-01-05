
  
  <script>
  export default {
    data() {
      return {
 
        inputText: '', // Testo inserito dall'utente
        transformedResult: '', // Testo trasformato
      };
    },
    methods: {
   
      transformText() {
        // Chiamata alla funzione che trasforma il testo inserito
        this.transformedResult = this.transformString();  
      },
      // Funzione per trasformare il testo 
      transformString() {
        let transformedStr = ''; // Variabile per memorizzare il testo trasformato
        let count = 1; // Contatore per contare le occorrenze delle lettere
        let str = this.inputText; // Otteniamo il testo direttamente dall'attributo inputText
  
        // Ciclo sul il testo inserito
        for (let i = 0; i < str.length; i++) {
          if (str[i] === str[i + 1]) { // Se la lettera corrente è uguale alla successiva
            count++; // Incrementa il contatore  
          } else {
            transformedStr += str[i]; // Aggiunge la lettera al testo trasformato
            if (count > 1) {
              transformedStr += count; // Aggiunge il numero se maggiore di 1
            }
            count = 1; // Reimposta il contatore per la prossima lettera
          }
        }
        return transformedStr; // Restituisce il testo trasformato
      },
    },
  };
  </script>
  
  <template>
    <h1>Quinto snack</h1>
      <div>
        <input v-model="inputText" placeholder="Inserisci il testo">
        
        <button @click="transformText()">Trasforma</button>
     
        <p>Risultato: {{ transformedResult }}</p>
      </div>
    </template>
  
  <style>

  </style>
  