<template>
    <div class="dizme_section">
               <div class="dizme_subscribe">
                   <div class="container">
                       <div class="inner">
                           <div class="background">
                               <div class="dots" data-img-url=""></div>
                               <div class="overlay"></div>
                           </div>
                           <div class="content">
                               <div class="left wow fadeInLeft" data-wow-duration="1s">
                                   <span class="subtitle">Subscribe Now</span>
                                   <h3 class="title">Get My Newsletter</h3>
                                   <p class="text">Get latest news, updates, tips and trics in your inbox</p>
                               </div>
                               <div class="right wow fadeInRight" data-wow-duration="1s">
                                   <div class="field">
                                       <input type="text" placeholder="Your email here">
                                       <input type="submit" value="Send Now" />
                                   </div>
                               </div>
                           </div>
                       </div>
                   </div>
               </div>
           </div>
   </template>
   
   
   <script>
   
   
   export default {
   name: "SubscriveComponent",
   }
   
   </script>
   
   <style scoped>
   
   .dizme_subscribe {
       width: 100%;
       height: auto;
       clear: both;
       background-color: #2b2d33;
       
   }
   
   .dizme_subscribe .inner {
       width: 85%;
       height: 299px;
       clear: both;
       position: relative;
       margin-left: 100px;
   }
   
   .dizme_subscribe .background {
       position: absolute;
       top: 0;
       bottom: 0;
       left: 0;
       right: 0;
       border-radius: 12px;
       background-image: url(@/assets/images/bg-newsletter.jpg);
       background-position: center;
   }
   
   .dizme_subscribe .background .dots {
       position: absolute;
       top: 0;
       bottom: 0;
       left: 0;
       right: 0;
       background-repeat: no-repeat;
       background-size: cover;
       background-position: center;
       border-radius: 12px
   }
   
   .dizme_subscribe .background .overlay {
       position: absolute;
       top: 0;
       bottom: 0;
       left: 0;
       right: 0;
       background-color: rgb(128, 103, 240, .92);
       z-index: 1;
       border-radius: 12px
   }
   
   .dizme_subscribe .content {
       position: relative;
       z-index: 2;
       display: flex;
       align-items: center;
       padding: 83px 90px 86px
   }
   
   .dizme_subscribe .left {
       width: 50%;
       padding-right: 40px
   }
   
   .dizme_subscribe .subtitle {
       display: inline-block;
       font-size: 21px;
       font-weight: 500;
       color: #fff;
       font-family: 'Jost', sans-serif;
       margin-bottom: 5px;
       padding-right: 250px;
   }
   
   .dizme_subscribe .title {
       color: #fff;
       font-size: 48px;
       margin-bottom: 10px;
       font-family: 'Jost', sans-serif;
   }
   
   .dizme_subscribe .text {
       color: #fff;
       font-family: 'Open Sans', sans-serif;
       padding-left: 15px;
   }
   


   .dizme_subscribe .right {
       width: 50%;
       padding-left: 10px
   }
   
   .dizme_subscribe .field {
       width: 100%;
       position: relative
   }
   
   .dizme_subscribe .field input[type=text] {
       width: 100%;
       height: 72px;
       border-radius: 12px;
       color: #6f6b80;
       background-color: #fff;
       padding-left: 30px;
   }
   
   .dizme_subscribe .field input[type=text]:focus {
       outline: none;
   }
   
   .dizme_subscribe .field input[type=submit] {
       position: absolute;
       right: 0;
       top: 0;
       height: 72px;
       border-top-right-radius: 12px;
       border-bottom-right-radius: 12px;
       color: #fff;
       font-family: 'jost', sans-serif;
       font-size: 18px;
       font-weight: 500;
       background-color: #f75023;
       padding: 0 35px;
   }
   
   
   </style>