<template>
 <input v-model="start" placeholder="Expression"/>
 <button @click="convertNum">Compute</button>
 <button @click="changeMode">Switch Mode</button>
 <p>Mode: {{ mode }}</p>
 <p>Result: {{ result }}</p>
</template>

<script>
import zeppo from 'zeppo';
export default {
  
  name: 'NumConverter',
  data() {
    
    return {
       start: '',
       result: '',
       mode: 'bin'
    };
  },
  methods: {
    changeMode(){
        if (this.mode === 'bin'){
            this.mode = 'dec';
        }
        else {
            this.mode = 'bin';
        }
    },
    convertNum(){
        if (this.mode === 'bin'){
            if (zeppo.isBin(this.start) === true){
                this.result = zeppo.binToDec(this.start);
            }
            else {
                this.result = 'You fucking moron rofl.'
            }
        }
        else {
            if (zeppo.isInt(this.start) === true){
                this.result = zeppo.decToBin(this.start);
            }
            else {
                this.result = 'You fucking moron rofl.'
            }
        }
    }
  }  
}
</script>