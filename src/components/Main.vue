<script>
export default{
   name:"Main",
  data(){
    return{

    }
  }
}
</script>

<template>

<main>
 <!--container start-->   
<div class="container">

 <!--box 1 start -->
 <div class="box1">
    <div class="left">
        <span>EVERYTHING IN MAXCOACH</span>
        <h2>Learn about Work Culture at MaxCoach</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam, iusto magni ad laudantium itaque adipisci!</p>
        <span>Have questions? <b>Get Free Guide <i class="fa-solid fa-arrow-right"></i></b> </span>
    </div>

    <div class="right">
    <img src="../../public/images/stock-full-hd-10-ohki1ayywq3cqutettrncduujpoaorifqu4relt2ts.jpg" alt="">
   <img src="../../public/images/about-us-01-ohkia3qg98rq9vg3s0mn2hkflr1migdqdw370qnegc.jpg" alt="">
    </div>
 </div>
<!--box 1 end -->

<!--box 2 start-->
<div class="box2">
    <div class="left">
      <img src="../../public/images/icon-youtube-play.png" alt="">   
     <img src="../../public/images/stock-full-hd-11-670x450.jpg" alt="">
    </div>

    <div class="right">
        <span>HOW WE WORK</span>
        <h2>Upgrade Your Skills Upgrade Your Life</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam, iusto magni ad laudantium itaque adipisci!</p>
        <span>Download <b>free guideback <i class="fa-solid fa-arrow-right"></i></b> </span>
    </div>
</div>
<!--box 2 end-->




</div>
<!--container end-->  
</main>

</template>

<style lang="scss" scoped>
.container{
    border:1px solid blue;
    max-width:850px;
    margin-left: auto;
    margin-right: auto;
}

/*box1 start*/
.box1{
    border: 1px solid red;
    display: flex;
    
    /*left side start*/
.left{
    padding-top: 20px;
    padding-right: 20px;
    display: flex;
    flex-direction: column;
    gap: 20px;


}
    /*left side end*/


    /*right side start*/
    .right{
       /* border: 1px solid red;*/
        position: relative;
        padding: 20px;
        img:nth-child(1){
           width: 350px;
           height: auto;
        }

        img:nth-child(2){
        position: absolute;
        top: 0;
        right: 0;
           width: 130px;
           height: auto;
        }
    }
    /*right side end*/
}
/*box1 end*/
/*------------------------------------------------------------------------------------------*/
/*box 2 start*/
.box2{
 border: 1px solid red;
 padding-top: 30px;
 padding-bottom: 30px;
  display: flex;
  gap: 40px;

   .left{
    position: relative;
    img:nth-child(1){
        width: 70px;
        position: absolute;
        left: 200px;
        top: 130px;
    }

    img:nth-child(2){
        width: 450px;
    }
   }

   .right{
    display: flex;
    flex-direction: column;
    gap: 20px;

   }
   
}
/*box 2 end*/
/*------------------------------------------------------------------------------------------*/



</style>