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
    <header>
   <div class="nav">
    <!--lista opzioni generata tramite props-->
    <ul>
        <li v-for="option in options">{{ option }}</li>
    </ul>

     <img src="../../public/images/dark-logo.png" alt="">

   <div class="search-profile-cart">
    <i class="fa-solid fa-cart-shopping"></i>
    <i class="fa-solid fa-user"></i>
    <div>
    <input type="search" placeholder="Search">
    <button><i class="fa-solid fa-magnifying-glass"></i></button>
    </div>
    
   </div>

   </div>
</header>
</template>

<style scoped lang="scss">

header{
    background-color: white;
    padding-top: 30px;
    padding-bottom: 30px;
}

.nav{
    
    max-width: 1000px;
    margin-left: auto;
    margin-right: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: black;

    ul{
        display: flex;
        justify-content: space-between;
        gap: 30px;
        list-style-type: none;

    }

    img{
        width: 120px;
        height: auto;    
    }

    .search-profile-cart{
        display: flex;
        justify-content: space-between;
        align-items: center;
        gap: 20px;
    }
}

</style>