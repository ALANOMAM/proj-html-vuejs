<script>
export default{
   name:"Footer",

   props:{
    options2:Array,
    socialOptions2: Array,
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
 

    <ul>
        <li v-for="social in socialOptions2"> <img :src="social" alt=""></li>
    </ul>
    
 </div>

</template>

<style lang="scss" scoped>

.footer-nav{
    max-width: 900px;
    margin-left: auto;
    margin-right: auto;
    display: flex;
    justify-content: space-between;
    


    ul{
        list-style-type: none;
    }
}

</style>