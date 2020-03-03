<template>
  <div id="app">
    <app-header></app-header>
    <router-view></router-view>
<!--     <PageContent v-bind:itemsList='itemsListInput'></PageContent> -->
    <app-footer></app-footer>
  </div>
</template>

<script>
//Registering components Locally
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
//import PageContent from './components/PageContent.vue'

export default {
  name: 'App',
  components: {
    //Registering with a name
    'app-header':Header,
    'app-footer':Footer,
    //Registering without a name
//    PageContent,
  },
  data() {
    return {
      itemsListInput: [{name:'Eggs',image:'./assets/eggs.jpg',show:false},
                    {name:'Bread',image:'/assets/bread.jfif',show:false},
                    {name:'Jam',image:'/assets/jam.jfif',show:false},
                    {name:'CornFlakes',image:'/assets/cornflakes.jfif',show:false},
                    {name:'Milk',image:'/assets/milk.jfif',show:false},
                    {name:'Juice',image:'/assets/juice.jfif',show:false}],
      msg: "Grocery"
    }
  }
}
</script>

<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
