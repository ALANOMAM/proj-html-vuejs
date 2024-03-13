<script>
export default{
   name:"Footer",

   props:{
    options2:Array,
    socialOptions2: Array,
   },

  data(){
    return{
        userEmail:'',
        mailOutput:''
    }
  },

  methods:{
    message(){
        /*console.log(this.userEmail)*/
        this.mailOutput = this.userEmail

    }
  }
}
</script>

<template>
  <footer>

 <div class="top-footer">

   <div class="top-container">
  <h2> Subscribe <span>Newsletters</span></h2>
  <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.  blanditiis autem, 
    numquam est! Distinctio ad modi ullam 
    deserunt voluptate officiis itaque nulla enim odit.</p>

    
   <div>
    <input type="search" placeholder="Enter your email" @keyup.enter="message()" v-model="userEmail">
    <button @click="message()">Subscribe</button>
   </div>
    <p :class="this.mailOutput.length == 0 ? '': 'mailConfirmVisible'" class="mailConfirmInvisible"> Thanks, we will be updating you using the mail: <span>{{this.mailOutput}}</span></p>
    </div>
       
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
b
</template>

<style lang="scss" scoped>
.mailConfirmInvisible{
    color: black;
    opacity: 0;
}

.mailConfirmVisible{
    opacity:1;
}

/*top footer inizio*/
.top-footer{

    background-color: white;

    .top-container{
        padding-bottom: 60px;
        padding-top: 60px ;
        max-width: 1200px;
        margin-left: auto;
        margin-right: auto;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 20px;
   background-image: url("../../public/images/maxcoach-shape-02.png"),url("../../public/images/maxcoach-shape-05.png");
   background-position: right bottom , left center;
   background-size: 100px , 100px;
   background-repeat: no-repeat, no-repeat;

        p{
            text-align: center;
        }
    }
     h2{
      color:black;
      font-size: 25px;
     }

     p{
        color:black ;
        max-width: 800px;
     }
    span{
        color:rgba(32, 173, 150, 1);
    }

    input{
        padding-right: 200px;
        padding-top:10px ;
        padding-bottom:10px ;
        padding-left:10px ;
        background-color: rgba(245, 245, 245, 1);
        border: 1px solid rgba(245, 245, 245, 1);
        border-top-left-radius: 4px;
        border-bottom-left-radius: 4px;
    }

    button{
        padding:10px;
        color: white;
        background-color:rgba(32, 173, 150, 1) ;
        border: 1px solid rgba(32, 173, 150, 1);
        border-radius: 4px;
        border-top-left-radius: 0;
        border-bottom-left-radius: 0;
    }
}
/*top footer fine*/

/*bottom footer inizio*/
.bottom-footer{
    background-color: rgba(23, 22, 33, 1);
    padding: 30px;


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

}
/*bottom footer fine*/
</style>