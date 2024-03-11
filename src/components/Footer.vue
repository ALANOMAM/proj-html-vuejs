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
  <footer>

 <div class="top-footer">
 7
 </div>   


<div class="bottom-footer">
  <div class="footer-nav">

  <div class="options-box">
    <!--popolato le varie opzioni con i props-->
    <ul v-for="option2 in options2">
        <li><strong>{{ option2.Title }}</strong></li>
        <li v-for="element in option2.elements ">{{element }}</li>
    </ul>  
  </div>

 <div class="socials">
    <div v-for="social in socialOptions2"> <img :src="social" alt=""></div>
 </div>

 
  </div>

   <div class="bottom">
    <span>2020 Maxcoach, All Rights Reserved</span>
    <i class="fa-solid fa-arrow-up"></i>
  </div>

</div>

</footer>

</template>

<style lang="scss" scoped>

.bottom-footer{
    background-color: rgba(23, 22, 33, 1);
    padding: 30px;
}

.footer-nav{
    max-width: 900px;
    margin-left: auto;
    margin-right: auto;    
}

.options-box{
    display: flex;
    justify-content: space-between;
    


    ul{
        list-style-type: none;
        display: flex;
        flex-direction: column;
        gap: 10px;
    }
}

.socials{
    display: flex;
    gap: 30px;
}

.bottom{
    display: flex;
    justify-content:space-between;
    align-items: center;
    margin-left: 700px;
    i{
        width: 70px;
        height: 70px;
        border-radius: 50%;
        font-size: 30px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color:rgba(32, 173, 150, 1);
       
    }
}

</style>