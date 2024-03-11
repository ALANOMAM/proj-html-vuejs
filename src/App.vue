<script>
import Header from "./components/Header.vue"
import Main from "./components/Main.vue"
import Footer from "./components/Footer.vue"

export default{
 components:{
  Header,
  Main,
  Footer,
 },

  data(){
    return{
      headerOptions:["Home","Pages","Courses","Features","Blog","Shop"],

    }
  }
}
</script>

<template>
  <Header :options="headerOptions"></Header>
  <Main></Main>
  <Footer></Footer>
</template>

<style>


</style>
