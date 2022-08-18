
<template>
    <div>
      <h1 style="color:#42B983;">Arithmetc Operations</h1>
      <p style="color:red;">Enter two integers:</p>
      <label>a: </label>
      <input type="number" v-model="input1"><br><br>
      <label>b: </label>
      <input type="number" v-model="input2"><br><br>
      <button @click="add">Add </button><br><br> 
      <button @click="sub">Subtract </button><br><br>
      <button @click="mult">Multiply</button><br><br>
      <button @click="div">Divide</button><br><br>
      <input v-if="result>0" type="text" v-model="result" class="positive">
      <input v-else type="text" v-model="result" class="negative">
    </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
 data(){
  return{
    num1:'',
    num2:'',
    sum:'',
    diff:'',
    prod:'',
    ratio:'',
    result:''
  }
 },
 methods:{
  add() {
    this.result = (Number(this.input1)+Number(this.input2));

  },
  sub(){
    this.result = (Number(this.input1)-Number(this.input2));

  },
  mult(){
    this.result = (Number(this.input1) * Number(this.input2));
  },
  div(){
    this.result = (Number(this.input1) / Number(this.input2));
  }
 },
}
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42B983;
}
.positive{
  color: green
}
.negative{
  color: red
}
</style>
