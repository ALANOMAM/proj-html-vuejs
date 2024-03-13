<script>
export default{
   name:"Header",
   props:{
     options1: Array,
   },

  data(){
    return{

    }
  }
}
</script>

<template>
    <header>
      <!--top header start-->  
     <div class="top-header"> 
   <div class="nav">
    <!--lista opzioni generata tramite props-->
    <ul>
        <li v-for="option1 in options1">{{ option1 }} <i class="fa-solid fa-chevron-down"></i> </li>
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
   </div>
   <!--top header end--> 

   <!--bottom header start-->
   <div class="bottom-header">
   <span>Commence Business</span>
   <h1>Distant Mentoring Program</h1>
   <button>Download Free Guidebook <i class="fa-solid fa-arrow-right"></i></button>
   </div>
   <!--bottom header end-->

    <!--header side options start-->
    <div class="side-options">
        <i class="fa-solid fa-play"></i>
        <i class="fa-regular fa-circle-xmark"></i>
        <i class="fa-solid fa-book"></i>
        <i class="fa-solid fa-cart-shopping"></i>   
    </div>

    <!--header side options end-->


</header>
</template>

<style scoped lang="scss">


header{
    height: 500px;
    background-image: url("../../public/images/home-3-hero-bg.jpg");
    background-position: center;
    background-size: cover;
}

.top-header{
    /*border: 1px solid blue;*/
    background-color: white;
    padding-top: 30px;
    padding-bottom: 30px;
}

/*nav start*/
.nav{
    /*border:1px solid red;*/
    max-width: 1200px;
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

        li{
            padding: 10px;
            display: flex;
            align-items: center;
            gap: 5px;
            i{
                font-size: 10px;
            }
        }

        li:hover{
            background-color: gray;
            border-radius: 5px;
            color: white;
        }

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

        input{
            padding: 10px;
            border-radius: 4px;
            border-bottom-right-radius: 0;
            border-top-right-radius:0;
            border-right:none ;
            background-color: rgba(245, 245, 245, 1);
            border: 1px solid rgba(245, 245, 245, 1);
        }

        button{
            padding: 10px;
            border-left: none;
            border-bottom-right-radius: 4px;
            border-top-right-radius:4px;
            background-color: rgba(245, 245, 245, 1);
            border: 1px solid rgba(245, 245, 245, 1);
        

          i{
            color: rgba(32, 173, 150, 1);
          } 
        }
    }

}
/*nav end*/

/*bottom header start*/
.bottom-header{
   /* border:1px solid red;*/
   margin-top: 100px;
   display: flex;
   flex-direction: column;
   align-items: center;
  
 span{ 
    font-weight: bold;
    font-size: 20px;
 }

 h1{
     
    font-weight:lighter;
 }

    button{
        margin-top: 20px;
        padding: 10px 20px;
        border-radius: 5px;
        border: 1px solid rgba(255, 255, 255, 1);
        background-color: rgba(255, 255, 255, 1);
        color: rgba(32, 173, 150, 1);

    }
}
/*bottom header end*/

/*side options start */
.side-options{
    position: absolute;
    right: 0;
    top: 200px;
    width: 30px;
    padding: 10px;
    border-radius: 3px;
    border: 1px solid white;
    background-color: white;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
i{
    color: black;
}
}
/*side options end */

</style>