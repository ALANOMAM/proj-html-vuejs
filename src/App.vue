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
      footerOptions:[
        {
          Title:'Address',
          elements:[
            "382 NE 191st St # 87394 Miami, FL 3317-3345",
            "+1(305)547-9909(9am-5pm EST,Monday-Friday)",
            "support@maxcoach.com"]
        },

        {
          Title:'Explore',
          elements:["Start here","Blog","About us","Success story","Courses","Contact us"]
        },

        {
          Title:'Information',
          elements:["Membership","Purchase guide","Privacy policy","Terms of service"]
        }

      ],

      footerSocials:["../../public/images/footer-facebook.png","../../public/images/footer-youtube.png","../../public/images/footer-twitter.png","../../public/images/footer-pinterest.png"],
    }
  }
}
</script>

<template>
  <Header :options1="headerOptions"></Header>
  <Main></Main>
  <Footer :options2="footerOptions" :socialOptions2="footerSocials"></Footer>
</template>

<style>


</style>
