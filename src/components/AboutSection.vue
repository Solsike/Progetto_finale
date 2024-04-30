<template>
<section id="about">
    <div class="container">
        <div class="row">
            <div class="col-lg-6 about_left">
                <img src="@/assets/images/img_about.jpg" alt="" class="img_about">
                <div class="years_box d-flex badge" ref="counter1Ref" v-show="isVisible1">
                    <h3>{{ counter1 }}</h3>
                    <p class="pe-5">Years of <br> Success</p>
                </div>
                <div class="projects_box d-flex badge" ref="counter2Ref" v-show="isVisible2">
                    <h3>{{ counter2 }}K</h3>
                    <p>Total <br> Projects</p>
                </div>
            </div>
            <div class="col-lg-6 d-flex flex-column about_right ps-5">
                <div class="designer d-flex">
                    <h4 :class="{ 'animated-paragraph': scrolled }">I'm a Designer</h4> 
                </div>
                <div class="designer_down d-flex">
                    <h2 :class="{ 'animated-paragraph': scrolled }">I Can Design Anything You Want</h2>
                </div>
                <div class="text_about d-flex" :class="{ 'animated-paragraph': scrolled }">
                    <p>Hello there! I'm a web designer, and I'm very passionate and dedicated to my work. With 20 years experience as a professional web developer, I have acquired the skills and knowledge necessary to make your project a success. I enjoy every step of the design process, from discussion and collaboration.</p>
                </div>
                <div class="btn_about d-flex"  :class="{ 'animated-paragraph': scrolled }">
                    <a class="buttonTwo orange-button" href="#contact"><button class="slide_from_top2 rounded-pill HimeMe">Hire Me</button></a>
                </div>
            </div>
            <div>
                <img src="@/assets/images/riccio_giallo.png" alt="" class="riccio_giallo">
                <img src="@/assets/images/macchia_viola.png" alt="" class="macchia_viola">
            </div>
        </div>
    </div>
</section>
</template>



<script scoped>
export default {
  name: 'AboutSection',
  data () {
    return {
        counter1: 0,
        counter2: 0,
        isVisible1: false,
        isVisible2: false
    }
  },
  mounted() {
      window.addEventListener('scroll', this.handleScroll); 
    },
    methods: {
      handleScroll() {
        if (!this.isVisible1 && this.isElementInViewport(this.$refs.counter1Ref)) {
          this.isVisible1 = true; 
          this.autoIncrement(this.$refs.counter1Ref, 'counter1'); 
        }
        if (!this.isVisible2 && this.isElementInViewport(this.$refs.counter2Ref)) {
          this.isVisible2 = true; 
          this.autoIncrement(this.$refs.counter2Ref, 'counter2', 250); 
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
      autoIncrement(target, counter, intervalDuration = 90) {
        const interval = setInterval(() => {
          if (this[counter] < 18 && counter === 'counter1') {
            this[counter]++;
          } else if (this[counter] < 9 && counter === 'counter2') {
            this[counter]++; 
          } else {
            clearInterval(interval); 
          }
        }, intervalDuration); 
      }
    }
  }
  
</script>




<style>

.transitionDiv{
    transition: transform 0.5s ease; 
}

.animated-paragraph {
      animation: moveUp 2s ease forwards; /* Animazione di movimento */
    }


    @keyframes moveUp {
      0% { transform: translateY(0); }
      100% { transform: translateY(-20px); }
    }










#about{
     background-color: #2a2d34;
     padding-top: 290px;
     padding-left: 15px;
     padding-bottom:150px;
     position: relative;
}



.img_about{
    width: 490px;
}

.years_box{
    position: absolute;
    width: 185px;
    height: 115px;
    background-color: #4b4f5c;
    top: 34%;
}

.years_box h3{
    color: #1cbe59;
    font-size: 50px;
    font-family: 'Jost',sans-serif;
    padding: 22px 20px 0 12px;
}

.years_box p{
    color: #fff;
    font-family: 'Jost',sans-serif;
    font-size: 18px;
    font-weight: 500;
    padding-top: 28px;
    line-height: 1.3;

}

.projects_box{
    position: absolute;
    width: 190px;
    height: 87px;
    background-color: #4b4f5c;
    border-radius: 5%;
    top: 57.5%;
    left: 34%;
}

.projects_box h3{
    color: #f0c45c;
    font-size: 50px;
    font-family: 'Jost',sans-serif;
    padding-top: 10px;
    padding-left: 20px;
}

.projects_box p{
    color: #fff;
    font-family: 'Jost',sans-serif;
    font-size: 18px;
    padding-right: 30px;
    padding-top: 19px;
    padding-left: 16px;
   text-align: left;
   font-weight: 500;
   line-height: 1.2;
}

.about_right{
    padding-top: 18px;
    padding-left: 40px;
}

.designer{
    color: #f75023;
  font-size: 24px;
  font-weight: 500;
  font-family: 'Jost',sans-serif;
  margin-bottom: 6px;
}

.designer_down h2{
    line-height: 1.25;
    color: #fff;
    font-family: 'Jost',sans-serif;
    font-weight: 500;
    font-size: 40px;
    margin-right: 180px;
    text-align: left; 
}

.text_about p{
    color: #6f6b80;
    font-family: 'Open sans',sans-serif;
    line-height: 30px;
    font-weight: 400;
    text-align: left;
    margin-right: 155px;
    padding-top: 15px;

}


.btn_about{
    padding-top: 20px;
    
}

.orange-button button.slide_from_top2 {
    background-color: #f75023;
    border: 2px solid #f75023;
    position: relative;
    z-index: 1;
    overflow: hidden;
    text-align: center;
    font-size: 16px;
    font-weight: 500px;
    font-family: 'Jost', sans-serif;
    color: white;
    padding: 10px 32px;
    margin-left: 18px;
}

.orange-button button.slide_from_top2::after {
    left: 0;
    right: 0;
    top: -100%;
    bottom: 100%;
    transition: all 0.55s;
    background-color: transparent;
}



.orange-button button.slide_from_top2:hover::after {
    background-color: #2b2d33;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    transition: all 0.35s;

}


.riccio_giallo{
    position: absolute;
    top: 9%;
    left: 2.5%;
}

.macchia_viola{
    position: absolute;
    right: 1%;
    bottom: 17%;
}
</style>