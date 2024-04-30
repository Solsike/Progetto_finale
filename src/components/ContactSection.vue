<template>
    <section class="dizme_section" id="contact">
        <div class="contact">
            <div class="container">
                <div class="title" data-align="center">
                    <span>Contact Me</span>
                    <h3>I Want To Hear From You</h3>
                    <p>Please fill out the form on this section to contact with me. Or call between 9:00 a.m. and
                        8:00 p.m. ET, Monday through Friday</p>
                </div>
                <div class="brush_1"><img src="https://marketifythemes.net/html/dizme/img/brushes/contact/1.png" alt />
                </div>
                <div class="contact_inner">
                    <div class="left">
                        <ul>
                            <li>
                                <div class="list_inner">
                                    <div class="icon map">
                                        <i class="fas fa-location-dot"></i>
                                    </div>
                                    <div class="short">
                                        <h3>Address</h3>
                                        <span>20, Somewhere in world</span>
                                    </div>
                                </div>
                            </li>
                            <li>
                                <div class="list_inner">
                                    <div class="icon envelope">
                                        <i class="far fa-envelope"></i>
                                    </div>
                                    <div class="short">
                                        <h3>Email</h3>
                                        <span><a href="#">
                                            <span class="__cf_email__"
                                                    data-cfemail="2b434e4747446b4f4251464e05484446">&#160;hello@dizme.com</span></a></span>
                                    </div>
                                </div>
                            </li>
                            <li>
                                <div class="list_inner">
                                    <div class="icon phone">
                                        <i class="fas fa-phone"></i>
                                    </div>
                                    <div class="short">
                                        <h3>Phone</h3>
                                        <span>+123 456 7890</span>
                                    </div>
                                </div>
                            </li>
                        </ul>
                    </div>
                    <div class="right">
                        <div class="fields">
                            <form action="/" method="post" class="contact_form" id="contact_form" autocomplete="off">
                                <div class="returnmessage"
                                    data-success="Your message has been received, We will contact you soon."></div>
                                <div class="alert_notice"><span>Please Fill Required Fields</span></div>
                                <div class="input_list">
                                    <ul>
                                        <li><input id="name" type="text" placeholder="Your Name" /></li>
                                        <li><input id="email" type="text" placeholder="Your Email" /></li>
                                        <li><input id="phone" type="tel" placeholder="Your Phone" /></li>
                                        <li><input id="subject" type="text" placeholder="Subject" /></li>
                                    </ul>
                                </div>
                                <div class="message_area">
                                    <textarea id="message" placeholder="Write your message here"></textarea>
                                </div>
                                <div class="button">
                                    <a id="send_message" href="#" class="rounded-pill"><span>Submit Now</span></a>
                                </div>
                            </form>
                        </div>
                    </div>
                    
                    <div class="brush_2"><img src="https://marketifythemes.net/html/dizme/img/brushes/contact/2.png"
                            alt />
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>


<script>


export default {
    name: "ContactSection",
}

</script>

<style scoped>

.dizme_section{
    background-color:#2b2d33 ;
}
.title span {
    font-size: 22px;
    font-weight: 500;
    color: #f75023;
    font-family: 'Jost', sans-serif;
    display: inline-block;
    margin-bottom: 6px;
}

.title h3 {
    font-size: 38px;
    line-height: 1.25;
    margin-bottom: 23px;
    font-family: 'Jost', sans-serif;
    color: white;

}

.title p{
    font-family: 'Open Sans', sans-serif;
    text-align: center;
    margin: 20px 50px;
}


.title {
    width: 100%;
    max-width: 680px;
    height: auto;
    clear: both;
    text-align: center;
    margin: 0 auto
}

.contact {
    width: 100%;
    height: auto;
    padding-top: 190px;
    padding-bottom: 200px;
}

.contact .contact_inner {
    width: 100%;
    display: flex;
    margin-top: 80px;;
    position: relative;
}

.contact .brush_1 {
    position: absolute;
    top:1150%;
    left: 0%;
}


.contact .left {
    width: 45%;
  margin-left: 50px ;
}

.contact .left ul {
    margin: 5;
    list-style-type: none
}

.contact .left ul li {
    margin: 0 0 10px
}

.contact .left ul li:last-child {
    margin-bottom: 0
}

.contact .left .list_inner {
    display: flex;
   text-align: left;
   padding-left: 10px;
}

.short h3{
    color: white;
    font-family: 'Jost', sans-serif;
    padding-left: 10px;
}

.short span{
    padding-left: 5px;
}

.contact .left .icon {
    width: 88px;
    height: 88px;
    border-radius: 100%;
    position: relative
}

.contact .left .icon i {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size: 24px
}

.contact .left .short {
    padding-left: 19px;
}


.contact .left .short  a{
    text-decoration: none;

}

.short span {
    color: #aca9bb;
}

.contact .right {
    width: 50%
}

.contact .fields {
    width: 100%;
    height: auto;
    padding-right: 100px;
}


.map{
    background-color:#fedfd7;
    border-radius: 50%;
    size: 50px;

}

.fa-location-dot{
    color: #f75023;
}

.envelope{
    background-color:#ddf5e6;
    border-radius: 50%;
    size: 50px;
}

.fa-envelope{
    color: #1cbe59;
}

.phone{
    background-color:#ece8fd;
    border-radius: 50%;
    size: 50px;
}

.fa-phone{
    color:#8067f0 ;
}

.contact .input_list {
    width: 100%;
    height: auto;

}

.contact .input_list ul {
    margin: 0 0 0 -40px;
    list-style-type: none
}

.contact .input_list ul li {
    margin: 0 0 12px;
    width: 50%;
    float: left;
    padding-left: 12px;
}

.contact input {
    width: 100%;
    height: 58px;
    padding: 0 30px;
    background-color: transparent;
    border: 1px solid #aca9bb;
    border-radius: 12px;
    color: #aca9bb;
    font-size: 18px
}



.contact input:focus {
    background-color: transparent;
    outline: none
}


.contact .message_area {
    width: 100%;
    margin-bottom: 4px
}

.contact .message_area textarea {
    width: 100%;
    height: 200px;
    padding: 16px 30px 30px;
    background-color: transparent;
    border: 1px solid #aca9bb;
    border-radius: 12px;
    color: #aca9bb;
    font-size: 18px
}

.contact .message_area textarea:focus {
    background-color: transparent;
    outline: none;

}

.contact .alert_notice {
    color: #f52225;
    margin-bottom: 7px;
    display: none;
    text-align: left;
    font-weight: 500
}

.contact .contact_error {
    color: #f52225;
    text-align: left;
    font-weight: 500
}

.contact .returnmessage {
    color: #3a00ff;
    margin-bottom: 7px;
    text-align: left;
    font-weight: 500
}



.button {
    width: 200px;
    height: auto;
    clear: both;
    float: left;
}

.button a {
    text-decoration: none;
    color: #fff;
    display: inline-block;
    font-family: "Jost", sans-serif;
    font-weight: 500;
    border: 2px solid #f75023;
    padding: 14px 35px 13px;
    position: relative;
    overflow: hidden
}

.button span {
    position: relative;
    z-index: 2;
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    -ms-transition: all .3s ease;
    -o-transition: all .3s ease;
    transition: all .3s ease
}

.button a:before {
    position: absolute;
    content: "";
    z-index: 0;
    background-color: #f75023;
    left: -5px;
    right: -5px;
    bottom: -5px;
    height: 110%;
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    -ms-transition: all .3s ease;
    -o-transition: all .3s ease;
    transition: all .3s ease;
   
}

.button a:hover:before {
    height: 0;

}

.button a:hover span {
    color: #fff;
}

p {
    color: #aca9bb;
}


.contact .brush_2 {
    position: absolute;
    bottom: -100px;
    right: 20px;
}




</style>