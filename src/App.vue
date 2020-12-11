<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Simple Vue Youtube Link Player"/>      
        <props2 linkss/>
        
        <input type="text" v-model.lazy="links" class="inp_link">

        <Head props3 msgVideo/>
        
        <p id="demo">{{ links }}</p>
      
        <iframe :src="links" v-bind="links" width="500px" height="300px">
        </iframe>

        <div id="example-2">
 
  <button v-on:click="ChangeBG" class="dark-btn">Dark-Theme</button>
</div>
<br><br>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Head from './components/Header.vue'

export default {
  name: 'App',
  
  components: {
    HelloWorld,
    Head,
     
  

 
  },

        data()
  {
      return{
      links: 'https://youtube.com/embed/hkpkxq8WGSA'
    }
    
  },
methods: {
    ChangeBG: function() {
      document.body.style.backgroundColor = "#1d1d1d",
      document.getElementById("app").style.color="#ffffff"
      alert("Dark Theme enabled")

    }
  }
    
}

</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.inp_link{
padding:10px;
border:2px solid #2da2d8;
border-radius:10px;
width:400px;
}
span{
  color:grey;
}
.dark-btn{
padding:10px;
margin-top:15px;
border-radius:10px;
border:none;
color:#ffffff;
background:purple;
font-family:calibri;
font-size:16px;
cursor:pointer;

}
</style>
