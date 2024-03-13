
<script>


export default{
   name:'CourseSlider',

   data(){
    
    return{

       /*course array start*/
        courseSlides:[
      [
   {
     image:"../../public/images/course-02-480x298.jpg",
     price:"$40.00",
     description:"Learning to Write as a Professional Author",
     lessons:" 20 Lessons",
     students:"50 Students"
   },

   {
    image:"../../public/images/stock-full-hd-03-480x298.jpg",
    price:"$20.00",
    description:"Customer-centric Info-Tech Strategies",
    lessons:" 26 Lessons",
    students:"40 Students"
   },

   {
    image:"../../public/images/stock-full-hd-04-480x298.jpg",
    price:"$16.00",
    description:"Open Programming Courses for Everyone: Python",
    lessons:" 40 Lessons",
    students:"60 Students"
   },

],


[
   {
     image:"../../public/images/course-featured-image-01-480x298.jpg",
     price:"$100.00",
     description:"Social Media Manager",
     lessons:" 10 Lessons",
     students:"20 Students"
   },

   {
    image:"../../public/images/stock-full-hd-11-670x450.jpg",
    price:"$70.00 ",
    description:"Data Analitics",
    lessons:" 30 Lessons",
    students:"30 Students"
   },

   {
    image:"../../public/images/stock-full-hd-06-480x298.jpg",
    price:"$16.00",
    description:"Wordpress Developer",
    lessons:" 40 Lessons",
    students:"60 Students"
   },

],


[
   {
     image:"../../public/images/artist-blog-03-480x325.jpeg",
     price:"$200.00",
     description:"Artist",
     lessons:" 12 Lessons",
     students:"24 Students"
   },

   {
    image:"../../public/images/artist-blog-01-480x325.jpg",
    price:"$700.00 ",
    description:"Artist",
    lessons:" 36 Lessons",
    students:"3 Students"
   },
  
   /*
   {
    image:"../../public/images/artist-blog-02-480x325.jpg",
    price:"$18.00",
    description:"Artist",
    lessons:" 400 Lessons",
    students:"60 Students"
   }, */

],





],
/*course array end*/

     // mi salvo una variabile dove memorizzo quale sia la slide attiva
     displayIndex: 0,

    }

   },

   methods:{
    backward(){
        this.displayIndex--
        console.log("display 1")

        if (this.displayIndex < 0) {
            this.displayIndex = this.courseSlides.length - 1;
        }
    },

    forward(){
        this.displayIndex++
        console.log("display 2")

        if(this.displayIndex >= this.courseSlides.length ){
        this.displayIndex = 0
      }

    }

  }


}
</script>


<template>

<section class="section3">
 <!--container start-->   
 <div class="container">
<!--box 3 start-->
<div class="box3">
<div class="titolo3">
    <span>JOIN MAXCOACH AT BEST </span>
    <h2>Latest Online <span class="mark">Courses</span></h2>
</div>

<!--course box  start-->
<div  v-for="(slide,index) in courseSlides" v-show="displayIndex === index"  class="courses-box" >
<div v-for="course in slide"  class="courses" >
<img :src="course.image" alt="">
<span class="mark"><b>{{ course.price }}</b></span>
<P>{{course.description }}</P>

<div class="stats">
<span> <i class="fa-regular fa-file"></i>  {{ course.lessons }}</span>
<span> <i class="fa-regular fa-user"></i> {{ course.students }}</span>
</div>
</div>
</div>
<!--course box  end-->



 <div class="selectButtons"> 
    <button class="display1" @click="backward()"> <i class="fa-solid fa-arrow-left"></i> PREVIOUS </button> 
    <button class="display2" @click="forward()"> NEXT <i class="fa-solid fa-arrow-right"></i> </button> 
</div>


</div>
<!--box 3 end-->
</div>
<!--container end-->  
</section>

</template>

<style lang="scss">

.container{
    color: black;
    /*border:1px solid blue;*/
    max-width:930px;
    margin-left: auto;
    margin-right: auto;
}

.mark{
    color:rgba(32, 173, 150, 1)  ;
}


.section3{
    background-color:rgba(248, 248, 248, 1) ;
}
/*box 3 start*/
.box3{
    padding:40px;
     .titolo3{
        display: flex;
        flex-direction: column;
        align-items: center;
     }

    .selectButtons{
        display: flex;
        justify-content: center;
        padding-top: 20px;
        gap: 40px;

        button{
            padding: 10px 20px;
            background-color:rgba(32, 173, 150, 1) ;
            border: 1px solid rgba(32, 173, 150, 1);
            border-radius: 5px;
            color: white;
        }

        button:active{
            background-color: green;
        }
    }


    .courses-box{
     margin-top: 40px;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    .courses{
        display: flex;
        flex-direction: column;
        gap:10px;
        margin-bottom: 20px;
        
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

/*box 3 end*/



</style>
