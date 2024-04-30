<template>
<section id="service">
    <div class="container">
        <div class="row">
            <div class="col service-text text-center">
                <h4>Services</h4>
                <h2>What I Do for Clients</h2>
                <p>Most common methods for designing websites that work well on desktop is responsive and adaptive design</p>
            </div>
        </div>
        <div class="row">
            <div class="col-lg-6">
                <a class="link-modal" @click="showModale_One = true" >
                    <div class="box_1 d-flex justify-content-around" >
                    <div class="icon">
                        <img src="@/assets/images/service_box_1.png" alt="" class="service_bubble img-one">
                        <i class="fa-solid fa-sitemap"></i>              
                    </div>
                    <div class="text-box text-start ps-5">
                        <h3>Creative Design</h3>
                        <h5>Starts from <span class="price">$99</span></h5>
                        <p>Web design refers to the design of websites that are displayed on the internet. It usually refers to the user experience aspects of website development</p>                    
                    </div>
                    <div v-if="showModale_One" class="modal-mask" @click.stop="closeModal">
                                <div class="modal-container">
                                     <img src="@/assets/images/creative_img.jpg" alt="" class="img-modale">
                                    <h3>Creative Design</h3>
                                    <h5>Starts from <span>$99</span></h5>
                                    <p>Dizme is a leading web design agency with an award-winning design team that creates innovative, effective websites that capture your brand, improve your conversion rates, and maximize your revenue to help grow your business and achieve your goals.</p>
                                    <p>In today’s digital world, your website is the first interaction consumers have with your business. That's why almost 95 percent of a user’s first impression relates to web design. It’s also why web design services can have an immense impact on your company’s bottom line.</p>
                                    <p>That’s why more companies are not only reevaluating their website’s design but also partnering with Kura, the web design agency that’s driven more than $2.4 billion in revenue for its clients. With over 50 web design awards under our belt, we're confident we can design a custom website that drives sales for your unique business.</p>
                                </div>
                                <button class="exit-button btn badge" click="closeModal" style="float: right;"><i class="fa-solid fa-xmark"></i></button>
                    </div>
                </div>
            </a>
            <a class="link-modal" @click="showModale_Two = true">
                <div class="box_2 d-flex justify-content-around">
                    <div class="icon">
                        <img src="@/assets/images/service_box_2.png" alt="circle" class="service_bubble img-two">
                        <i class="fa-regular fa-address-card"></i>
                        
                    </div>
                    <div class="text-box text-start ps-5">
                        <h3>UI/UX Design</h3>
                        <h5>Starts from <span class="price">$299</span></h5>
                        <p>Web design refers to the design of websites that are displayed on the internet. It usually refers to the user experience aspects of website development</p>                    
                    </div> 
                    <div v-if="showModale_Two" class="modal-mask" @click.stop="closeModal_Two">
                            <div class="modal-container">
                                     <img src="@/assets/images/uiux_img.jpg" alt="ux design" class="img-modale">
                                    <h3>UI/UX Design</h3>
                                    <h5>Starts from <span>$299</span></h5>
                                    <p>Dizme is a leading web design agency with an award-winning design team that creates innovative, effective websites that capture your brand, improve your conversion rates, and maximize your revenue to help grow your business and achieve your goals.</p>
                                    <p>In today’s digital world, your website is the first interaction consumers have with your business. That's why almost 95 percent of a user’s first impression relates to web design. It’s also why web design services can have an immense impact on your company’s bottom line.</p>
                                    <p>That’s why more companies are not only reevaluating their website’s design but also partnering with Kura, the web design agency that’s driven more than $2.4 billion in revenue for its clients. With over 50 web design awards under our belt, we're confident we can design a custom website that drives sales for your unique business.</p>
                                </div>
                                <button class="exit-button btn badge" click="closeModal" style="float: right;"><i class="fa-solid fa-xmark"></i></button>
                        </div>           
                </div> 
            </a>                               
            </div>
            <div class="col-lg-6">
                <a class="link-modal" @click="showModale_Three = true">
                  <div class="box_3 d-flex justify-content-around">
                    <div class="icon">
                        <img src="@/assets/images/service_box_3.png" alt="circle" class="service_bubble img-three">
                        <i class="fa-solid fa-atom"></i>
                    </div>
                    <div class="text-box text-start ps-5">
                        <h3>Graphic Design</h3>
                        <h5>Starts from <span class="price">$199</span></h5>
                        <p>Web design refers to the design of websites that are displayed on the internet. It usually refers to the user experience aspects of website development</p>                    
                    </div> 
                    <div v-if="showModale_Three" class="modal-mask" @click.stop="closeModal_Three">
                            <div class="modal-container">
                                     <img src="@/assets/images/graphic_img.jpg" alt="graphic design" class="img-modale">
                                    <h3>Graphic Design</h3>
                                    <h5>Starts from <span>$199</span></h5>
                                    <p>Dizme is a leading web design agency with an award-winning design team that creates innovative, effective websites that capture your brand, improve your conversion rates, and maximize your revenue to help grow your business and achieve your goals.</p>
                                    <p>In today’s digital world, your website is the first interaction consumers have with your business. That's why almost 95 percent of a user’s first impression relates to web design. It’s also why web design services can have an immense impact on your company’s bottom line.</p>
                                    <p>That’s why more companies are not only reevaluating their website’s design but also partnering with Kura, the web design agency that’s driven more than $2.4 billion in revenue for its clients. With over 50 web design awards under our belt, we're confident we can design a custom website that drives sales for your unique business.</p>
                                </div>
                                <button class="exit-button btn badge" click="closeModal" style="float: right;"><i class="fa-solid fa-xmark"></i></button>
                        </div>
                </div>  
                </a>
                <a class="link-modal" @click="showModale_Four = true">
                 <div class="box_4 d-flex justify-content-around">
                    <div class="icon">
                        <img src="@/assets/images/service_box_4.png" alt="" class="service_bubble img-four">
                        <i class="fa-regular fa-window-maximize"></i>
                    </div>
                    <div class="text-box text-start ps-5">
                        <h3>Web Design</h3>
                        <h5>Starts from <span class="price">$399</span></h5>
                        <p>Web design refers to the design of websites that are displayed on the internet. It usually refers to the user experience aspects of website development</p>                    
                    </div> 
                    <div v-if="showModale_Four" class="modal-mask" @click.stop="closeModal_Four">
                            <div class="modal-container">
                                     <img src="@/assets/images/web_img.jpg" alt="graphic design" class="img-modale">
                                    <h3>Web Design</h3>
                                    <h5>Starts from <span>$399</span></h5>
                                    <p>Dizme is a leading web design agency with an award-winning design team that creates innovative, effective websites that capture your brand, improve your conversion rates, and maximize your revenue to help grow your business and achieve your goals.</p>
                                    <p>In today’s digital world, your website is the first interaction consumers have with your business. That's why almost 95 percent of a user’s first impression relates to web design. It’s also why web design services can have an immense impact on your company’s bottom line.</p>
                                    <p>That’s why more companies are not only reevaluating their website’s design but also partnering with Kura, the web design agency that’s driven more than $2.4 billion in revenue for its clients. With over 50 web design awards under our belt, we're confident we can design a custom website that drives sales for your unique business.</p>
                                </div>
                                <button class="exit-button btn badge" click="closeModal" style="float: right;"><i class="fa-solid fa-xmark"></i></button>
                        </div>
                </div>   
                </a>              
            </div>
        </div>
    </div>
    <div class="container">
        <img src="@/assets/images/service-img-2.png" alt="" class="ServiceImg_2">
    </div>
</section>
</template>




<script>
export default({
  name: 'ServiceSection',
  data() {
    return {
      showModale_One: false,
      showModale_Two: false,
      showModale_Three: false,
      showModale_Four: false

    };
  },
  methods: {
    closeModal() {
      this.showModale_One = false;
    },
    closeModal_Two() {
        this.showModale_Two = false;
    },
    closeModal_Three() {
        this.showModale_Three = false;
    },
    closeModal_Four() {
        this.showModale_Three = false;
    }
  }
});
</script>










<style scoped>


#service{
    background-color: #2b2d33;
    padding-top: 150px;
    padding-bottom: 150px;
    background-image: url('@/assets/images/service-img-1.png');
    background-repeat: no-repeat;
    background-position-y: 265px;
    background-size: 460px;
    position: relative;
}

.ServiceImg_2{
position: absolute;
left: 69.5%;
top: -2%;;
}

.service-text h2{
    color: white;
    font-family: 'Jost',sans-serif;
    font-weight: 500;
    font-size: 38px
}


.service-text h4{
    color:#f75023;
    font-family: 'Jost',sans-serif;
    font-weight: 500;
    font-size: 22px;
}

.service-text p{
    color: #b0acc0;
    font-family: 'Open Sans', sans-serif;
    font-size: 16px;
    line-height: 30px;
    margin: 0 375px;
    padding-top: 10px;
}

.box_1,
.box_2,
.box_3,
.box_4{
width: 530px;
height: 370px;
border-radius: 3%;
background-color: #4b4f5c;
}

.box_1,
.box_3{
    margin-bottom: 30px;
    margin-top: 80px;
}

.box_1,
.box_2{
    margin-left: 100px;
}


.service_bubble{
padding-top: 60px;
padding-left: 60px;

}



.text-box{
    padding-right: 30px;
    padding-top: 60px;
}

.text-box h3{
color: white ;
font-family: 'Jost', sans-serif;
font-size: 25px;
}

.text-box h5{
    color: white;
    font-size: 18px;
    padding-top: 6px;
    padding-bottom: 18px;
    font-family: 'Jost', sans-serif;
}

.price{
color: #f75023;
}

.text-box p{
    font-family: 'Open Sans',sans-serif;
    color:#b0acc0;
    font-size: 16px;
    text-align:left;
    line-height: 30px;
    
}

.img-one{
position: relative;
}

.fa-sitemap{
    position: absolute; 
    font-size: 40px;
   color: rgba(0, 0, 0, 0.856);
    left: 19.5%;
    top: 36%;
}

.img-two{
    position: relative;
}

.fa-address-card{
    position: absolute;
    font-size: 40px ;
    color: #2b2d33;
    left:19.5%;
    top: 67%;
}


.img-three{
    position: relative;
}

.fa-atom{
    position: absolute;
    font-size: 50px;
    color: #2b2d33;
    left: 56.2%;
    top: 36%;
}


.img-four{
    position: relative;
}

.fa-window-maximize{
    position: absolute;
    font-size: 40px;
    color: #2b2d33;
    left: 56.5%;
    top:67%;
}



/* FINESTRE MODALI */

.link-modal{
    cursor: pointer;
    text-decoration: none;
}



.modal-mask {
  position: fixed;
  z-index: 9999;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, .9);
  display: flex;
  align-items: center;
  justify-content: center;

}

.modal-container {
  background-color: #34353a;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.651);
  width: 800px;
  height: 600px;
  overflow-y: auto;
}



.modal-container::-webkit-scrollbar {
width: 8px;
}
.modal-container::-webkit-scrollbar-track {
background-color: transparent;
}
.modal-container::-webkit-scrollbar-thumb {
background-color:#777;
}

.exit-button{
   background-color: transparent;
   border: 2px solid white;
   padding:10px 12px;
   margin-bottom: 560px;
   margin-left: 20px;
   border-radius: 27%;
   transition: all 0.3s ease;
}


.exit-button:hover{
    border: 2px solid white;
    border-radius: 50%;
    transition: all 0.2s ease;

}

.fa-xmark{
    font-size: 18px;
    color: white;
}

.modal-container h3{
    color: white;
    font-size: 30px;
    font-weight: 500;
  line-height: 1.3;
  font-family: 'Jost',sans-serif;
  text-align: left;
  padding-left: 50px;
  padding-top: 30px;
}

.modal-container h5{
    font-weight: 500;
  font-size: 21px;
  color: white;
  font-family: 'Jost',sans-serif;
  text-align: left;
  padding-left: 50px; 
    padding-bottom: 20px;
}

.modal-container span{
    color: #f75023;
 
}

.modal-container p{
color: #b9b5c9;
text-align: left;
font-family: 'Open Sans', sans-serif;
font-size: 16px;
font-weight: 400;
line-height: 30px;
margin-right: 25px;
margin-left: 50px;

}



.img-modale{
border-radius: 2%;
width: 700px;
height: 450px;
padding-top: 45px;


}



</style>