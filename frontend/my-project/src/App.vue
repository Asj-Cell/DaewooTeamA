<template>
  <div>
    <HelloWorld/>
  </div>
  <nav>
    <router-link to="/">Home</router-link>
    <router-link to="/headerComponent">HeaderComponent</router-link>
  </nav>
    <router-view/>
</template>
<script>
import HelloWorld from './components/HelloWorld.vue'
export default {

  name: 'App',

  components: {
    HelloWorld
  },

  data() {
    return {
      list: [],
      resultData: null,
    }
  },

  async mounted() {
    //const 결과 = await axios.get('https://jsonplaceholder.typicode.com/posts');
    this.list = this.resultData.data.result;
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
