<template class="main">
  <div class="form container mt-5">

    <h2>Enter the string you want to change</h2>
    <form @submit.prevent>
    <input type="text" v-model.lazy="input" id="value" class="input-group mb-3 pt-2 mt-3" required>
    <button @click="change" class="btn btn-dark" >Change String</button>    
    </form>

    <div id="view">
      <h3>Preview</h3>
      <p>Input String:{{input}}</p>
      <p>Output String:</p>
      
    </div>
  
  </div>
</template>

<script>
export default {

  
  name: 'HelloWorld',
  data(){
    return{
        input:"",
      
    }
  },
  methods:{
    change(){
        let temp=this.input
        let final=temp.toUpperCase();
        // alert("the updated string is "+final);
        var node = document.createElement("p");
        var textnode = document.createTextNode(final);
        node.appendChild(textnode);
        document.getElementById("view").appendChild(node);
}
  }
  
}

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.form{
      font-family: Arial, Helvetica, sans-serif;
      font-size: 100% ;
      
      background-color:#C0C0C0 ;
      text-align: center;

      
}

</style>
