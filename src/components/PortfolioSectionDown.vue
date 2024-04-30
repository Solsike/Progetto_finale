<template>
    <section id="portfoliodown">
    <div class="container down">
        <div class="row">
            <div class="col-lg-6 left">
                <h4>Design is Life</h4>
                <h2>I Develop Skills Regularly to Keep Me Update</h2>
                <p>Most common methods for designing websites that work well on desktop is responsive and adaptive design</p>
                <div class="illustrator">
                    <span class="progress-name">Illustrator</span>
                    <span class="valore one">85%</span>
                    <div class="progress" role="progressbar" aria-label="Success" aria-valuenow="20" aria-valuemin="0" aria-valuemax="80">
                            <div class="progress-bar orange" :style="{width: progressBarWidth1}"></div>
                            </div>
                </div>   
                <div class="photoshop">
                    <span class="progress-name">Photoshop</span>
                    <span class="valore two">95%</span>
                    <div class="progress " role="progressbar" aria-label="Info example" aria-valuenow="50" aria-valuemin="0" aria-valuemax="100">
                            <div class="progress-bar green bg-success" :style="{width: progressBarWidth2}"></div>
                            </div>
                </div>        
                <div class="figma">
                    <span class="progress-name">Figma</span>
                    <span class="valore three">75%</span>
                            <div class="progress" role="progressbar" aria-label="Warning example" aria-valuenow="75" aria-valuemin="0" aria-valuemax="100">
                            <div class="progress-bar purple" :style="{width: progressBarWidth3}" ></div>
                            </div>
                </div>  
            </div>
            <div class="col-lg-6 right">
                <img class="portfolio_img" src="@/assets/images/portfolio_img.jpg" alt="worker">
            </div>
        </div>
    </div>   
    </section>
    
  </template>
  
  <script>
  export default {
    name: 'PortfolioSectionDown',
    data() {
      return {
        progressBarWidth1: '0%',
        progressBarWidth2: '0%',
        progressBarWidth3: '0%',
        scrolled: false
      };
    },mounted () {
      window.addEventListener('scroll', this.handleScroll);
    },
    methods: {
      handleScroll() {
        if (!this.scrolled && this.isElementInViewport(document.querySelector('.progress'))) {
          setTimeout(() => {
            this.progressBarWidth1 = '85%'; 
            this.progressBarWidth2 = '95%'; 
            this.progressBarWidth3 = '75%'; 
          },200);
        
          this.scrolled = true; 
          window.removeEventListener('scroll', this.handleScroll); // Rimuove l'event listener per lo scroll dopo il primo scroll
        }
    },
    isElementInViewport(el) {
        const rect = el.getBoundingClientRect();
        return (
          rect.top >= 0 &&
          rect.left >= 0 &&
          rect.bottom <= (window.innerHeight || document.documentElement.clientHeight) &&
          rect.right <= (window.innerWidth || document.documentElement.clientWidth)
        );
      }, 
  }
}
  </script>
  


  <style scoped>

section{
    background-color: #2b2d33;
    background-image: url("@/assets/images/macchia_viola_2.png");
    background-repeat: no-repeat;
    background-position-x: 1150px;
    background-position-y: -190px;
}


  
h4{
    font-family: 'Jost',sans-serif;
    color:#f75023;
    font-size: 22px;
    font-weight: 500;
    letter-spacing: 0.5px;
}



  h2 {
    text-align: center;
    font-family: 'Jost',sans-serif;
    font-size: 38px;
    color: #fff; 
    margin: 13px 0;
}


p{
    font-family: 'Open Sans',sans-serif;
    color: #b9b5c9;
    font-size: 16px;
    line-height: 30px;
    margin: 0 120px;

}
  



/*sezione portofolio down*/

.down h4{
    font-size: 22px;
    padding-left: 7px;
}



.down h2{
    text-align: left;
    margin-right: 90px;
    padding-left: 7px;
}


.down p{
    text-align: left;
    margin: 10px 100px 0 0 ;
    padding-left: 7px;
}
.down{
    padding-top: 200px;
}



.left{
    text-align: left;
  padding-left: 110px;
  padding-top: 150px;
}


.progress{
    margin: 0 10px;
    width: 440px;
    height: 8px;
}

span{
    color: #fff;
    font-family: 'Jost',sans-serif;
    font-size: 18px;
  font-weight: 500;
  display: inline-block;
}

.progress-name{
    margin-top: 40px;
    margin-bottom: 10px;
    padding-left: 10px;
}

.valore{
    color: #f75023;
    float: right;
    margin-top: 40px;
    margin-bottom: 10px;
    padding-right: 110px;
    font-size: 16px;
}

.one{
margin-right:47px;
}

.orange{
    background-color: #f75023;
    
}

.three{
    margin-right: 90px;
}

.purple{
    background-color: #8067f0;
}


.portfolio_img{
    width: 450px;
}



  </style>