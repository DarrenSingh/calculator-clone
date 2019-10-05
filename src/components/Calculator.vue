<template>
  <div class="calculator">
    <h1 class="display">{{ current || '0' }}</h1>
    <!-- row 1 -->
    <span @click="clear" class="top">AC</span>
    <span class="top">+/-</span>
    <span @click="sign" class="top">%</span>
    <span @click="sign" class="operator">&#247;</span>
    <!-- row 2 -->
    <span @click="addDigit('7')">7</span>
    <span @click="addDigit('8')">8</span>
    <span @click="addDigit('9')">9</span>
    <span class="operator">	&#215;</span>
    <!-- row 3 -->
    <span @click="addDigit('4')">4</span>
    <span @click="addDigit('5')">5</span>
    <span @click="addDigit('6')">6</span>
    <span class="operator">	&#8722;</span>
    <!-- row 3 -->
    <span @click="addDigit('1')">1</span>
    <span @click="addDigit('2')">2</span>
    <span @click="addDigit('3')">3</span>
    <span class="operator">+</span>
    <!-- row 4 -->
    <span @click="addDigit('0')" class="zero">0</span>
    <span @click="addDecimal()">.</span>
    <span class="operator equals">=</span>
  </div>
</template>

<script>

export default {
  data(){
    return {
      current: ''
    }
  },
  methods:{
    clear(){
      this.current = '';
    },
    sign(){

    },
    percent(){

    },
    multiply(){

    },
    divide(){

    },
    add(){

    },
    subtract(){

    },
    addDigit(int){
      this.current += int;
    },
    addDecimal(){
      if(!this.current.includes(".")){
        this.current += ".";
      }
    }
  }
}
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .calculator{
    display: grid;
    grid-template-columns: repeat(4,1fr);
    grid-auto-rows: minmax(50px,auto);
    color: white;
    max-width: 400px;
    margin:auto;
  }

  .display{
    grid-column: 1/5;
    background-color: rgba(102,101,71,0.45);
    border: 1px solid grey;
    height: 100px;
    text-align: right;
    font-size: 5rem;
    font-weight: 100;
    padding:20px;
    margin:0px;
    overflow:scroll;
    border-radius: 10px 10px 0px 0px;
    color: white;
    }

  .zero{
    grid-column:1/3;
    border-radius: 0px 0px 0px 10px;

  }

  .equals{
    border-radius: 0px 0px 10px 0px;
  }

  .operator{
    background-color: rgb(111,203,159);	
  }
  .operator:hover{
    background-color: rgb(122,213,169);
  }
  .operator:active{
    background-color: rgb(116,208,164);
  }

  .top{
    background-color: rgb(48,46,62);
  }

   .top:hover{
    background-color: rgb(58,56,72);
  }
   .top:active{
    background-color: rgb(53,51,67);
  }

  span{
    border: 1px solid rgba(102,101,71,0.5);
    border-collapse: collapse;
    line-height: 80px;
    font-size: 1.5em;
    background-color: rgb(80,78,83);
  }
  span:hover{
    background-color: rgb(90,88,93);
  }
  span:active{
    background-color: rgb(85,83,88);
  }




</style>
