<template>
    <div class="backgroundHome">
          <section id="homeDown" class="transitionDiv" :class="{ 'animated-paragraph': scrolled }">
        <div class="container">
            <div class="row ">
                <div class="col-lg-4 box_red">
                    <div>
                        <img src="@/assets/images/homeDown_1.png" alt="brushes" class="homeDownBrush">
                       <img src="https://marketifythemes.net/html/dizme/img/svg/process/target-2.svg" alt="" class="svg-target">
                    </div>
                    <div><h3>Pixel Perfect</h3></div>
                    <div><p>Most common methods for designing websites that work well on desktop is responsive and adaptive design.</p></div>
                </div>
                <div class="col-lg-4 box_green">
                    <div>
                        <img src="@/assets/images/homeDown_2.png" alt="brushes" class="homeDownBrush">
                        <img src="https://marketifythemes.net/html/dizme/img/svg/process/brush-2.svg" alt="" class="svg-brush">
                    </div>
                   
                    <div><h3>High Quality</h3></div>
                    <div><p>Most common methods for designing websites that work well on desktop is responsive and adaptive design.</p></div>
                </div>
                <div class="col-lg-4 box_yellow">
                    <div>
                        <img src="@/assets/images/homeDown_3.png" alt="brushes" class="homeDownBrush">
                        <img src="https://marketifythemes.net/html/dizme/img/svg/process/energy-2.svg" alt="" class="svg-light">
                    </div>
                    <div><h3>Awesome Idea</h3></div>
                    <div><p>Most common methods for designing websites that work well on desktop is responsive and adaptive design.</p></div>
                </div>
            </div>
        </div>
    </section> 
    </div>
 
</template>


<script>
export default {
  name: 'HeaderSectionDown',
  data() {
      return {
        scrolled: false // Flag per indicare se è stato effettuato lo scroll
      };
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll); // Aggiunta dell'event listener per lo scroll
    },
    methods: {
      handleScroll() {
        this.scrolled = true; // Imposta il flag scrolled a true quando viene effettuato lo scroll
        window.removeEventListener('scroll', this.handleScroll); // Rimuove l'event listener per lo scroll dopo il primo scroll
      }
    }
  }

</script>









<style scoped>

/*homeDown */

.backgroundHome{
    background-color: #2b2d33;
    padding-bottom: 10px;
}



.transitionDiv{
    transition: transform 0.5s ease; 
}

.animated-paragraph {
      animation: moveUp 3s ease forwards;
      padding-bottom: 10px; /* Animazione di movimento */
    }


    @keyframes moveUp {
      0% { transform: translateY(0); }
      100% { transform: translateY(-20px); }
    }



#homeDown{
    background-color: #2b2d33;
    padding-top: 200px;
    position: relative;
}

.homeDownBrush{
    max-width: 90px;
}

h3{
    color: #e4e4e5;
    padding: 25px 0 15px;
    font-size: 24px;
    font-weight: 500;
  line-height: 1.3;
  font-family:'Jost',sans-serif;
}

p{
    color: #a7a4b6;
    margin-left: 60px;
    margin-right: 50px;
    font-family: 'Open sans',sans-serif;
    line-height: 30px;
    letter-spacing: 0;
    font-weight: 400;
    font-size: 16px;


}

.box_red{
    padding-left: 50px;
    padding-right: 0px;
    
}


.svg-target{
   width: 50px;
   position: absolute;
   top: 45%;
    left: 21%;
}


.svg-brush{
    position: absolute;
    width: 48px;
    top: 46.5%;
    left: 48.5%;
    
}


.box_yellow{
    padding-right:50px;
    padding-left: 0px;
}

.svg-light{
    position: absolute;
    width: 49px;
    top:46%;
    left: 75.7%;
}

</style>