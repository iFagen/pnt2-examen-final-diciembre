<template>

    <h3>NT2 – Exámen Final (Diciembre)</h3>
    <hr>
    <label> Color: </label>
    <input type="text" v-model="color">
    <label> Fondo: </label>
    <input type="text" v-model="fondo">
    <label> Tamaño: </label>
    <input type="text" v-model="tamanio">

  <hr>
    <label>Texto: </label>
    <input type="text" v-model="texto" :style="{color: color ,background: fondo ,fontSize: tamanio}">
    <p>Cantidad de palabras {{cantPalabras()}}</p>

  <br>  
  <h3>Multiple Choice</h3>
  <hr>
  <table class="table">
    <tr>
      <th>Número de pregunta</th>
      <th> Respuesta</th>
    </tr>

    <tr>
      <td>1</td>
      <td>B</td>
    </tr>
    <tr>
      <td>2</td>
      <td>C</td>
    </tr>
    <tr>
      <td>3</td>
      <td>B</td>
    </tr>
    <tr>
      <td>4</td>
      <td>D</td>
    </tr>
    <tr>
      <td>5</td>
      <td>C,D</td>
    </tr>
  </table>

</template>

<script>
export default {
  name: 'Proyecto',
  data(){
    return{
      color:"",
      fondo:"", 
      tamanio:"",
      texto:"",

    }
  },
  methods:{
    cantPalabras(){
      let text = this.texto.trim() 
      if(text.split("").length != 0) {
        text = text.split(" ")
        console.log(text);
      }
      return  text.length
    }
  },
  computed:{
  }
}
</script>


<style scoped lang="css">
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
  color: #42b983;
}
</style>
