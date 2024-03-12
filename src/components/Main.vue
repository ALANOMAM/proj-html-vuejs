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
        <h2>Learn about <span class="mark">Work Culture</span> at MaxCoach</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam, iusto magni ad laudantium itaque adipisci!</p>
        <span>Have questions? <span class="mark"><b>Get Free Guide <i class="fa-solid fa-arrow-right"></i></b></span> </span>
    </div>

    <div class="right">
    <img src="../../public/images/stock-full-hd-10-ohki1ayywq3cqutettrncduujpoaorifqu4relt2ts.jpg" alt="">
   <img src="../../public/images/about-us-01-ohkia3qg98rq9vg3s0mn2hkflr1migdqdw370qnegc.jpg" alt="">
    </div>
 </div>
<!--box 1 end -->
</div>
<!--container end--> 




 <!--container start-->   
 <div class="container">
<!--box 2 start-->
<div class="box2">
    <div class="left">
      <img src="../../public/images/icon-youtube-play.png" alt="">   
     <img src="../../public/images/stock-full-hd-11-670x450.jpg" alt="">
    </div>

    <div class="right">
        <span>HOW WE WORK</span>
        <h2>Upgrade Your Skills <span class="mark">Upgrade Your Life</span></h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam, iusto magni ad laudantium itaque adipisci!</p>
        <span>Download <b>free guideback <i class="fa-solid fa-arrow-right"></i></b> </span>
    </div>
</div>
<!--box 2 end-->
</div>
<!--container end--> 



 <!--container start-->   
 <div class="container">
<!--box 4 start -->
<div class="box4">
    <div class="left">
        <span>TESTIMONIALS</span>
        <h2>Why Do People <span class="mark">*Hearts*</span> Us?</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam, iusto magni ad laudantium itaque adipisci!</p>
        <span> <b>View all <i class="fa-solid fa-arrow-right"></i></b> </span>
    </div>

    <div class="right">
        <div class="testimonial">
         <span><strong>Proffessional team of specialists and passionate mentors at reach</strong></span>
         <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet esse tempore praesentium laudantium delectus nihil.</p>
         <div class="img-description">
         <img src="../../public/images/testimonial-avata-01.jpg" alt="">
          <div class="description">
         <span><strong>MADLEY PONDOR</strong></span>
         <span>/ IT Specialist</span>
         </div>
         </div>
         </div>
   <!-- <img src="../../public/images/testimonial-avata-02.jpg" alt="">-->
    </div>
 </div>
<!--box 4 end -->
</div>
<!--container end--> 



 <!--container start-->   
 <div class="container">
<!--box 5 start-->
<div class="box5">
    <div class="left"> 
     <img src="../../public/images/home-3-team-image-300x278.png" alt="">
    </div>

    <div class="right">
        <span> EVERYTHING IN MAXCOACH</span>
        <h2>We'er Here To <span class="mark">Transform</span> You!</h2>
        <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Totam, iusto magni ad laudantium itaque adipisci!</p>
        <button>Get Free Guide</button>
    </div>
</div>
<!--box 5 end-->
</div>
<!--container end--> 



<section class="section6">
 <!--container start-->   
 <div class="container">
<!--box 6 start-->
<div class="box6">
<div class="titolo6">
    <span>READ FOR MORE JOYMENT</span>
    <h2>Latest From <span class="mark">Our Blogs</span></h2>
</div>

<div class="artist-box">

<div v-for="blog in latestBlogs"  class="artists">
<img :src="blog.image" alt="">
<span>{{ blog.work }}</span>
<P>{{blog.description }}</P>

<div class="stats">
<span><i class="fa-regular fa-calendar"></i>{{ blog.date }}</span>
<span><i class="fa-regular fa-eye"></i>{{ blog.views }}</span>
</div>
</div>

</div>

</div>
<!--box 6 end-->
</div>
<!--container end-->  
</section>

</main>

</template>

<style lang="scss" scoped>
main{
    background-color: white;
}
.container{
    color: black;
    border:1px solid blue;
    max-width:930px;
    margin-left: auto;
    margin-right: auto;
}

.mark{
    color:rgba(32, 173, 150, 1)  ;
}

/*box1 start*/
.box1{
    padding:40px;
    
    border: 1px solid red;
    display: flex;
   background-image: url("../../public/images/maxcoach-shape-02.png"),url("../../public/images/maxcoach-shape-07.png");
   background-position: right bottom ,  center;
   background-size: 100px , 100px;
   background-repeat: no-repeat, no-repeat;
    
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
padding:40px;  
 border: 1px solid red;
 padding-top: 30px;
 padding-bottom: 30px;
 background-image: url("../../public/images/maxcoach-shape-01.png"),url("../../public/images/maxcoach-shape-05.png");
   background-position: right center , left top;
   background-size: 100px , 100px;
   background-repeat: no-repeat, no-repeat;
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
    padding:40px;
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

       .testimonial{
        display: flex;
        flex-direction: column;
        gap:10px;
        .img-description{
             display: flex;
             align-items: center;
             gap: 20px;

             .description{
               display: flex;
               flex-direction: column;
               gap:10px;
             }

            img{
            width: 50px;
            height: auto;
            border-radius: 50%;
        }

        }
       
       }
    } 
    /*right side end*/
}
/*box4 end*/
/*--------------------------------------------------------------------------------------------*/

/*box 5 start*/
.box5{
 padding:40px;
 border: 1px solid red;
 padding-top: 30px;
 padding-bottom: 30px;
 background-image: url("../../public/images/maxcoach-shape-01.png"),url("../../public/images/maxcoach-shape-05.png"),url("../../public/images/maxcoach-shape-08.png");
   background-position: right center , left top, bottom center;
   background-size: 100px , 100px , 100px;
   background-repeat: no-repeat, no-repeat, no-repeat;
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
.section6{
    background-color:rgba(248, 248, 248, 1) ;
}
/*box 6 start*/
.box6{
    padding:40px;
     .titolo6{
        display: flex;
        flex-direction: column;
        align-items: center;
     }

    .artist-box{
    margin-top: 40px;
    display: flex;
    justify-content: space-between;
    .artists{
        display: flex;
        flex-direction: column;
        gap:10px;
        
        p{
            max-width: 250px;
        }
        
        img{
            width: 250px;  
        }

        .stats{
            display: flex;
            gap: 20px;
        }
        
    }
   }
}

/*box 6 end*/

</style>