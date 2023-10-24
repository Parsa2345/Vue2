<template>
  <img alt="Vue logo" src="./assets/logo.png" ref="img1">
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <Hello :name="name" :family="family" :phone="33454" @nameClicked="testRef"  ref="myCP">
  
  <template v-slot:name><h1>{{name}}</h1></template>
  <template v-slot:family><h1>{{family}}</h1></template>
  <template v-slot:phone><h1>1232314</h1></template>
  </Hello>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Hello from './components/Hello.vue'

export default {
  data() {
    return {
      name:"Mohsen",
      family:"Parsa",
    }
  },
  methods: {
    test(text){
      console.log("object   "+text );
      this.$refs.img1.remove();
    },
    testRef(){  
      this.$refs.myCP.myAlert2("Hasan");
    }


  },
  name: 'App',
  components: {
    // HelloWorld,
    Hello
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
</style>
