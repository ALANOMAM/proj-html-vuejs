<script>
export default{
   name:"Main",
  data(){
    return{
        latestBlogs:[
           {
             image:"../../public/images/artist-blog-03-480x325.jpeg",
             work:"ARTIST",
             description:"Brush Strokes Energize Trees in Painting",
             date:" May 15,2020",
             views:"688 views"
           },

           {
            image:"../../public/images/artist-blog-01-480x325.jpg",
             work:"ARTIST",
             description:"Pocket-Sized Notebooks Hold Miniature Paintings",
             date:" May 25,2020",
             views:"608 views"
           },

           {
            image:"../../public/images/artist-blog-02-480x325.jpg",
             work:"ARTIST",
             description:"Connection Between Self-Portraits and Identity",
             date:" Feb 15,2022",
             views:"300 views"
           }

        ]

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




<!--box 4 start -->
<div class="box4">
    <div class="left">
        <span>TESTIMONIALS</span>
        <h2>Why Do People Hearts Us?</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam, iusto magni ad laudantium itaque adipisci!</p>
        <span> <b>View all <i class="fa-solid fa-arrow-right"></i></b> </span>
    </div>

    <div class="right">
    <img src="../../public/images/testimonial-avata-01.jpg" alt="">
   <img src="../../public/images/testimonial-avata-02.jpg" alt="">
    </div>
 </div>
<!--box 4 end -->


<!--box 5 start-->
<div class="box5">
    <div class="left"> 
     <img src="../../public/images/home-3-team-image-300x278.png" alt="">
    </div>

    <div class="right">
        <span> EVERYTHING IN MAXCOACH</span>
        <h2>We'er Here To Transform You!</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam, iusto magni ad laudantium itaque adipisci!</p>
        <button>Get Free Guide</button>
    </div>
</div>
<!--box 5 end-->

<!--box 6 start-->
<div class="box6">
<div>
    <span>READ FOR MORE JOYMENT</span>
    <h2>Latest From Our Blogs</h2>
</div>

<div class="artist-box">

<div v-for="blog in latestBlogs"  class="artists">
<img :src="blog.image" alt="">
<span>{{ blog.work }}</span>
<P>{{blog.description }}</P>

<div class="stats">
<span><i class="fa-regular fa-calendar"></i>{{ blog.date }}</span>
<span><i class="fa-regular fa-eye"></i>{{blog.views}}</span>
</div>
</div>



</div>



</div>
<!--box 6 end-->


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

/*box4 start*/
.box4{
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
       /* border: 1px solid red;
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
        }*/
    } 
    /*right side end*/
}
/*box4 end*/
/*--------------------------------------------------------------------------------------------*/
/*box 5 start*/
.box5{
 border: 1px solid red;
 padding-top: 30px;
 padding-bottom: 30px;
  display: flex;
  gap: 40px;


   .right{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 20px;

    button{
        padding: 10px 30px;
        border-radius: 5px;
        background-color:rgba(32, 173, 150, 1) ;
        color:white;
        border: 1px solid rgba(32, 173, 150, 1);
    }

   }
   
}
/*box 5 end*/
/*------------------------------------------------------------------------------------------------------*/
/*box 6 start*/
.box6{

    .artist-box{
    display: flex;
    .artists{
        display: flex;
        flex-direction: column;
        gap:10px;
        img{
            width: 250px;  
        }

        .stats{
            display: flex;
            gap: 30px;
        }
        
    }
   }
}

/*box 6 end*/

</style>