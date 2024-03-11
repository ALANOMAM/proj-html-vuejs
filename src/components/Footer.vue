<script>
export default{
   name:"Footer",

   props:{
    options2:Array,
   },

  data(){
    return{

    }
  }
}
</script>

<template>

 <div class="footer-nav">
    <!--popolato le varie opzioni con i props-->
    <ul v-for="option2 in options2">
        <li><strong>{{ option2.Title }}</strong></li>
        <li v-for="element in option2.elements ">{{element }}</li>
    </ul>
    
 </div>

</template>

<style lang="scss" scoped>


</style>