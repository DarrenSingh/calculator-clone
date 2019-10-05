<template>
  <div class="calculator">
    <h1 class="display">{{ current || '0' }}</h1>
    <!-- row 1 -->
    <span class="top">AC</span>
    <span class="top">+/-</span>
    <span class="top">%</span>
    <span class="operator">\</span>
    <!-- row 2 -->
    <span>7</span>
    <span>8</span>
    <span>9</span>
    <span class="operator">X</span>
    <!-- row 3 -->
    <span>4</span>
    <span>5</span>
    <span>6</span>
    <span class="operator">-</span>
    <!-- row 3 -->
    <span>1</span>
    <span>2</span>
    <span>3</span>
    <span class="operator">+</span>
    <!-- row 4 -->
    <span class="zero">0</span>
    <span>.</span>
    <span class="operator">=</span>
  </div>
</template>

<script>
export default {
  data(){
    return {
      current: 0
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
  }

  .display{
    grid-column: 1/5;
    background-color: rgba(200,200,200,0.5);
    border: 1px solid grey;
    border-collapse: collapse;
    height: 125px;
    text-align: right;
    font-size: 5rem;
    font-weight: 100;
    padding-right:20px;
    margin:0px;
    overflow:scroll;
  }

  .zero{
    grid-column:1/3;
  }

  .operator{
    background-color: rgb(253,141,14);
    color:rgb(255,237,214)
  }

  .top{
    background-color: rgb(48,46,62);
  }

  span{
    border: 1px solid grey;
    border-collapse: collapse;
    line-height: 100px;
    background-color: rgb(80,78,83);
    color:rgb(255,237,214)
  }

</style>
