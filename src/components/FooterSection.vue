<template>
    <section id="footer">
        <div class="copyright">
            <div class="container">
                <div class="inner">
                    <div class="left">
                        <p>Developed with love by
                            <a href="https://themeforest.net/user/marketify" target="_blank">Marketify
                            </a> &copy; 2022
                        </p>
                    </div>
                    <div class="right">
                        <ul>
                            <li><a href="#">Terms &amp; Condition</a></li>
                            <li><a href="#">Privacy Policy</a></li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        <div class="scroll-button">
            <button class="scroll-to-top" @click="scrollToTop" v-if="showScrollButton">TO TOP</button>
                <div class="progress-container" v-if="showScrollButton">
                    <div class="progress-bar" :style="{ height: scrollPercentage + '%' }"></div>
            </div>           
        </div>
    </section>
</template>


<script>
export default {
    name: 'FooterSection',
    data() {
    return {
      scrollPercentage: 0,
      showScrollButton: false 
    };
  },
  mounted() {
    window.addEventListener('scroll', this.updateScrollProgress); 
  },
  methods: {
    updateScrollProgress() {
      const scrollHeight = document.documentElement.scrollHeight - window.innerHeight;
      const scrollTop = window.scrollY;
      this.scrollPercentage = (scrollTop / scrollHeight) * 100;
     
      this.showScrollButton = scrollTop > 200;
    },
    scrollToTop() {
      window.scrollTo({
        top: 0,
        behavior: 'smooth' 
      });
    }
  }
};
</script>


<style scoped>




/* parte sinistra */
.copyright {
    width: 100%;
    height: auto;
    background-color: #3f4453;
    padding: 57px 0 61px;
}

.copyright .inner {
    width: 100%;
    height: auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.copyright .left p {
    font-size: 16px;
    color: #b9b5c9;
    padding-left: 120px;
}

.copyright .left a {
    text-decoration: none;
    color: #b9b5c9;
    font-weight: 700;
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    -ms-transition: all .3s ease;
    -o-transition: all .3s ease;
    transition: all .3s ease;
}

.copyright .left a:hover {
    color: #f75023;
}


/* parte destra*/

.copyright .right ul {
    margin-right: 70px;
    list-style-type: none;
}

.copyright .right ul li {
    display: inline-block;
}



.copyright .right ul li a {
    text-decoration: none;
    color: #b9b5c9;
    font-size: 16px;
    margin-right: 50px;
    -webkit-transition: all .3s ease;
    -moz-transition: all .3s ease;
    -ms-transition: all .3s ease;
    -o-transition: all .3s ease;
    transition: all .3s ease;
}

.copyright .right ul li a:hover {
    color: #f75023;
}


/* scroll to top */


  
  .progress-container {
    position: fixed;
    animation: moveUp 0.3s ease forwards;
    bottom: 30px;
    right: 23px; 
    width: 0.5px; 
    height: calc(30% - 100px); 
    background-color:#36383f;
    z-index: 9999;

   
  }

  .progress-bar { 
    background-color:rgba(255, 255, 255, .4); 

  }


button {
    position: fixed;
    top: 70%;
    left: 98%;
    background-color: transparent;
    border: none;
    writing-mode: vertical-lr;
    color: white;
    font-size: 13px;
    font-family: 'Open Sans', sans-serif;
    animation: moveUp 0.3s ease forwards;

}

@keyframes moveUp {
      0% { transform: translateX(0); }
      100% { transform: translateX(-10px); }
      
    }


button::after {
    background-color: transparent;

}
</style>