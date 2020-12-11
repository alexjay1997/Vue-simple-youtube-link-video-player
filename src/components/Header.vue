<template>
  <div class="hello">
    <h4 props="msgVideo">Ex:https://www.youtube.com/embed/hkpkxq8WGSA</h4>
    
       <h3 props="linkss"> Enter youtube Link in embed format:</h3><!--this is props-->

  
  </div>
</template>

<script>

export default {
  name: 'Header',
  props: {
    msgVideo: String,
    linkss : String
   
   
  }
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
  color: #42b983;
}
#video{
width:500px;
height:350px;
border:1px solid red;
}
</style>
