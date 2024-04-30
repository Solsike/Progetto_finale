<template>
    <div class="section" id="blog">
        <div class="news">
            <div class="container">
                <div class="title" data-align="center">
                    <span>From My Blog</span>
                    <h3>Our Recent Updates, Blog, Tips, <br> Tricks &amp; More</h3>
                </div>
                <div class="news_list">
                    <ul>
                        <li class="up">
                            <a class="link-modal" @click="showModale_One = true">
                              <div class="list_inner">
                                <div class="image">
                                    <img src="https://marketifythemes.net/html/dizme/img/news/1.jpg" alt />
                                    
                                    <div class="date">
                                        <h3>23</h3>
                                        <span>Dec</span>
                                    </div>
                                    <a class="link" href="#"></a>
                                </div>
                                <div class="details">
                                    <span class="category"><a href="#">Web Development</a></span>
                                    <h3 class="title"><a href="#">Jim Morisson Says when the musics over turn off
                                            the light</a></h3>
                                </div>
                                <div class="news_details">
                                    <div class="news_hidden">
                                        <div class="text">
                                            <p>Dizme is a leading web design agency with an award-winning design
                                                team that creates innovative, effective websites that capture your
                                                brand, improve your conversion rates, and maximize your revenue to
                                                help grow your business and achieve your goals.</p>
                                            <p>In today’s digital world, your website is the first interaction
                                                consumers have with your business. That's why almost 95 percent of a
                                                user’s first impression relates to web design. It’s also why web
                                                design services can have an immense impact on your company’s bottom
                                                line.</p>
                                            <p>That’s why more companies are not only reevaluating their website’s
                                                design but also partnering with Kura, the web design agency that’s
                                                driven more than $2.4 billion in revenue for its clients. With over
                                                50 web design awards under our belt, we're confident we can design a
                                                custom website that drives sales for your unique business.</p>
                                        </div>
                                    </div>
                                </div>
                                <div v-if="showModale_One" class="modal-mask" @click.stop="closeModal">
                                <div class="modal-container">
                                     <img src="@/assets/images/blog_img1.jpg" alt="" class="img-modale">
                                    <h4>Jim Morisson Says when the musics over turn off the light</h4>
                                    <h6>Web Development</h6>
                                    <p>Dizme is a leading web design agency with an award-winning design team that creates innovative, effective websites that capture your brand, improve your conversion rates, and maximize your revenue to help grow your business and achieve your goals.</p>
                                    <p>In today’s digital world, your website is the first interaction consumers have with your business. That's why almost 95 percent of a user’s first impression relates to web design. It’s also why web design services can have an immense impact on your company’s bottom line.</p>
                                    <p>That’s why more companies are not only reevaluating their website’s design but also partnering with Kura, the web design agency that’s driven more than $2.4 billion in revenue for its clients. With over 50 web design awards under our belt, we're confident we can design a custom website that drives sales for your unique business.</p>
                                </div>
                                <button class="exit-button btn badge" click="closeModal" style="float: right;"><i class="fa-solid fa-xmark"></i></button>
                                </div>
                            </div>  
                            </a>                          
                        </li>
                        <li class="up">
                            <a class="link-modal" @click="showModale_Two = true">
                            <div class="list_inner">
                                <div class="image">
                                    <img src="https://marketifythemes.net/html/dizme/img/news/2.jpg" alt />

                                    <div class="date">
                                        <h3>23</h3>
                                        <span>Dec</span>
                                    </div>
                                    <a class="link" href="#"></a>
                                </div>
                                <div class="details">
                                    <span class="category"><a href="#">Branding</a></span>
                                    <h3 class="title"><a href="#">How to be appreciated for your hard work as a
                                            developer</a></h3>
                                </div>
                                <div class="news_details">
                                    <div class="news_hidden">
                                        <div class="text">
                                            <p>Dizme is a leading web design agency with an award-winning design
                                                team that creates innovative, effective websites that capture your
                                                brand, improve your conversion rates, and maximize your revenue to
                                                help grow your business and achieve your goals.</p>
                                            <p>In today’s digital world, your website is the first interaction
                                                consumers have with your business. That's why almost 95 percent of a
                                                user’s first impression relates to web design. It’s also why web
                                                design services can have an immense impact on your company’s bottom
                                                line.</p>
                                            <p>That’s why more companies are not only reevaluating their website’s
                                                design but also partnering with Kura, the web design agency that’s
                                                driven more than $2.4 billion in revenue for its clients. With over
                                                50 web design awards under our belt, we're confident we can design a
                                                custom website that drives sales for your unique business.</p>
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div v-if="showModale_Two" class="modal-mask" @click.stop="closeModal_Two">
                            <div class="modal-container">
                                     <img src="@/assets/images/blog_img2.jpg" alt="ux design" class="img-modale">
                                    <h4>How to be appreciated for your hard work as a developer</h4>
                                    <h6>Branding</h6>
                                    <p>Dizme is a leading web design agency with an award-winning design team that creates innovative, effective websites that capture your brand, improve your conversion rates, and maximize your revenue to help grow your business and achieve your goals.</p>
                                    <p>In today’s digital world, your website is the first interaction consumers have with your business. That's why almost 95 percent of a user’s first impression relates to web design. It’s also why web design services can have an immense impact on your company’s bottom line.</p>
                                    <p>That’s why more companies are not only reevaluating their website’s design but also partnering with Kura, the web design agency that’s driven more than $2.4 billion in revenue for its clients. With over 50 web design awards under our belt, we're confident we can design a custom website that drives sales for your unique business.</p>
                                </div>
                                <button class="exit-button btn badge" click="closeModal" style="float: right;"><i class="fa-solid fa-xmark"></i></button>
                        </div>       
                            </a>                     
                        </li>
                        <li class="up">
                            <a class="link-modal" @click="showModale_Three = true">
                              <div class="list_inner">
                                    <div class="image">
                                        <img src="https://marketifythemes.net/html/dizme/img/news/3.jpg" alt />
                                        <div class="date">
                                            <h3>23</h3>
                                            <span>Dec</span>
                                        </div>
                                        <a class="link" href="#"></a>
                                    </div>
                                    <div class="details">
                                        <span class="category"><a href="#">Social Media</a></span>
                                        <h3 class="title"><a href="#">How designers and developers can collaborate
                                                better</a></h3>
                                    </div>
                                    <div class="news_hidden">
                                        <div class="news_informations">
                                            <div class="text">
                                                <p>Dizme is a leading web design agency with an award-winning design
                                                    team that creates innovative, effective websites that capture your
                                                    brand, improve your conversion rates, and maximize your revenue to
                                                    help grow your business and achieve your goals.</p>
                                                <p>In today’s digital world, your website is the first interaction
                                                    consumers have with your business. That's why almost 95 percent of a
                                                    user’s first impression relates to web design. It’s also why web
                                                    design services can have an immense impact on your company’s bottom
                                                    line.</p>
                                                <p>That’s why more companies are not only reevaluating their website’s
                                                    design but also partnering with Kura, the web design agency that’s
                                                    driven more than $2.4 billion in revenue for its clients. With over
                                                    50 web design awards under our belt, we're confident we can design a
                                                    custom website that drives sales for your unique business.</p>
                                            </div>
                                        </div>
                                    </div>
                                    <div v-if="showModale_Three" class="modal-mask" @click.stop="closeModal_Three">
                            <div class="modal-container">
                                     <img src="@/assets/images/blog_img3.jpg" alt="graphic design" class="img-modale">
                                    <h4>How designers and developers can collaborate better</h4>
                                    <h6>Social Media</h6>
                                    <p>Dizme is a leading web design agency with an award-winning design team that creates innovative, effective websites that capture your brand, improve your conversion rates, and maximize your revenue to help grow your business and achieve your goals.</p>
                                    <p>In today’s digital world, your website is the first interaction consumers have with your business. That's why almost 95 percent of a user’s first impression relates to web design. It’s also why web design services can have an immense impact on your company’s bottom line.</p>
                                    <p>That’s why more companies are not only reevaluating their website’s design but also partnering with Kura, the web design agency that’s driven more than $2.4 billion in revenue for its clients. With over 50 web design awards under our belt, we're confident we can design a custom website that drives sales for your unique business.</p>
                                </div>
                                <button class="exit-button btn badge" click="closeModal" style="float: right;"><i class="fa-solid fa-xmark"></i></button>
                        </div>
                                </div>   
                            </a>
                           
                        </li>
                    </ul>
                </div>
            </div>
            <div class="brush_1"><img src="https://marketifythemes.net/html/dizme/img/brushes/news/1.png" alt /></div>
            <div class="brush_2"><img src="https://marketifythemes.net/html/dizme/img/brushes/news/2.png" alt /></div>
        </div>
    </div>

</template>






<script>
export default({
  name: 'BlogSection',
  data() {
    return {
      showModale_One: false,
      showModale_Two: false,
      showModale_Three: false

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
    }
  }
});
</script>
<style scoped>

.news{
    background-color: #2b2d33;
}


.title span {
    font-size: 24px;
    font-weight: 500;
    color: #f75023;
    font-family: 'jost', sans-serif;
    display: inline-block;
    margin-bottom: 6px;
}

.title h3 {
    font-size: 40px;
    line-height: 1.25;
    margin-bottom: 23px;
    font-family: 'Jost', sans-serif;
    color: white;
}


.title {
    width: 100%;
    max-width: 680px;
    height: auto;
    clear: both;
    text-align: center;
    margin: 0 auto
}


.news {
    width: 100%;
    height: auto;
    clear: both;
    float: left;
    padding-top: 120px;
    position: relative;
    padding-bottom: 150px;
}

.news .news_list {
    width: 100%;
    height: auto;
    clear: both;
    display: inline-flex;
    padding-top: 65px;
}

.news ul .main {
    margin: 0 0 0 0px;
    list-style-type: none
}

.news ul li {
    margin: 0 0 25px;
    width: 33.3333%;
    display: inline-flex;
    padding-left: 25px
}

.list_inner {
    width: 100%;
    clear: both;
    display: inline;
    position: relative;
}


.image{
    overflow: hidden;
    max-width:100%;
}

.image:hover{
    border-radius: 13px;
    transition: all .3s ease;
}




.image img {
    position: relative;
    width: 100%;
    border-radius: 13px;
   
}



.image img:hover {
    transform: scale(1.1);
    overflow: hidden;
    transition: all .3s ease;
    border-radius: 13px;
}



.date {
    position: absolute;
    top: 18px;
    right: 15px;
    z-index: 2;
    display: inline-block;
    background-color: #1cbe59;
    text-align: center;
    border-radius: 12px;
    padding: 15px 19px 9\px;
    line-height: 1;
}

.date span{
    color: white;
}

.date h3 {
    font-size: 24px;
    color: #fff; 
   margin-bottom: 0px;
   
}


.category a {
    font-size: 16px;
    color: #f75023;
    font-family: 'Jost', 'sans-serif';
    text-decoration: none;
    font-weight: 500;
    display: inline-block;
    margin-bottom: 2px;
    padding-right: 260px;
    padding-top: 20px;
}

.news ul li .details .title {
    line-height: 1.4;
    font-family: 'Jost', sans-serif;
    padding-left: 30px;
}

.title a {
    font-size: 21px;
    color: white;
    display: inline-block;
    text-decoration: none;
    text-align: left;
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    -ms-transition: all .3s ease;
    -o-transition: all .3s ease;
    transition: all .3s ease;
    
}

.news ul li .details .title a:hover {
    color: #f75023
}

.news .news_hidden {
    display: none;
    opacity: 0;
    visibility: hidden;
    position: absolute;
    z-index: -11
}


.news .brush_1 {
    position: absolute;
    top: 180px;
    left: 70px;
}

.news .brush_2 {
    position: absolute;
    top: -60px;
    right: 8px;
}


/* finestre modali */

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

.modal-container h4{
    color: white;
    font-size: 22px;
    font-weight: 500;
  line-height: 1.3;
  font-family: 'Jost',sans-serif;
  text-align: left;
  padding-left: 50px;
  padding-top: 30px;
}

.modal-container h6{
    font-weight: 500;
  font-size: 16px;
  color: white;
  font-family: 'Jost',sans-serif;
  text-align: left;
  padding-left: 50px; 
    padding-bottom: 20px;
    color: #b9b5c9;
    padding-top: 5px;
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