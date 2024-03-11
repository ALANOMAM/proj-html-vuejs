<script>
export default{
   name:"Header",
   props:{
     options: Array,
   },

  data(){
    return{

    }
  }
}
</script>

<template>
   <div class="nav">
    <!--lista opzioni generata tramite props-->
    <ul>
        <li v-for="option in options">{{ option }}</li>
    </ul>

   </div>
</template>

<style>


</style>