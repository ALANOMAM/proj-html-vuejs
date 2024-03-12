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

 <div class="box1">
    <div class="left">
        <span>EVERYTHING IN MAXCOACH</span>
        <h2>Learn about Work Culture at MaxCoach</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam, iusto magni ad laudantium itaque adipisci!</p>


    </div>

    <div class="right">
    <img src="../../public/images/stock-full-hd-10-ohki1ayywq3cqutettrncduujpoaorifqu4relt2ts.jpg" alt="">
   <img src="../../public/images/about-us-01-ohkia3qg98rq9vg3s0mn2hkflr1migdqdw370qnegc.jpg" alt="">
    </div>
   
 </div>

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
    
    /*left side start*/
.left{

}
    /*left side end*/


    /*right side start*/
    .right{
        border: 1px solid red;
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



</style>