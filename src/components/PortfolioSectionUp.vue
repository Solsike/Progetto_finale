<template>
    <section id="portfolio">
        <div class="container">
            <div class="row gy-5 gy-lg-0">
                <div class="col text-section">
                    <span>Portfolio</span>
                    <h3>My Amazing Works</h3>
                    <p>Most common methods for designing websites that work well on desktop <br>
                        is responsive and adaptive design
                    </p>
                    <div class="filterImages d-flex row justify-content-between">
                        <ul>
                            <li class="current"><a @click="filterImages('all')">All</a></li>
                            <li><a @click="filterImages('youtube')">Youtube</a></li>
                            <li><a @click="filterImages('vimeo')">Vimeo </a></li>
                            <li><a @click="filterImages('soundcloud')">Soundcloud</a></li>
                            <li> <a @click="filterImages('popup')">Popup</a></li>
                            <li><a @click="filterImages('detail')">Detail</a></li>
                        </ul>
                    </div>
                    <div class="gallery">
                        <div class="grid-container">
                            <div v-for="(image, index) in images" :key="index" :class="'image-' + index"
                                class="image-container">
                                <img class="image" :src="image.src" :alt="image.alt" :class="image.category"
                                    v-show="showImage(image.category)" @click="openModal(index)">
                            </div>
                            <div v-if="showModal" class="modal" tabindex="-1" role="dialog">
                                <div class="modal-dialog" role="document">
                                    <div class="modal-content">
                                          <div class="image-fluid"><img :src="images[currentIndex].src" class="image-fluid" alt="Modal Image"></div>
                                        <div class="modal-body">
                                         </div>   
                                            
                                         <button class="btn w3-display-left w3-btn" @click="plusDivs(-1)">
                                            <i class="fa-solid fa-caret-left"></i></button>
                                               
                                            
                                            <button class="btn w3-display-right w3-btn" @click="plusDivs(1)">
                                                <i class="fa-solid fa-caret-right"></i></button>
                                            <button class="btn btn-x" @click="closeModal"><i class="fa-solid fa-xmark"></i></button>   
                                        
                                    </div>
                                </div>
                                
                            </div>
                        </div>

                    </div>
                    <img class="yellow_brush" src="@/assets/images/macchia_gialla.png" alt="brushes yellow">
                </div>
            </div>
        </div> 
    </section>
</template>


<script scoped>
export default {
    name: "GallerySection",

    data() {
        return {

            images: [
                { src: require('@/assets/images/rombo_rosso.jpg'), alt: 'Immagine 1', category: 'youtube' },
                { src: require('@/assets/images/Vimeo.jpg'), alt: 'Immagine 2', category: 'vimeo' },
                { src: require('@/assets/images/Soundcloud.jpg'), alt: 'Immagine 3', category: 'soundcloud' },
                { src: require('@/assets/images/popup_1.jpg'), alt: 'Immagine 4', category: 'popup' },
                { src: require('@/assets/images/popup_2.jpg'), alt: 'Immagine 5', category: 'popup' },
                { src: require('@/assets/images/detail.jpg'), alt: 'Immagine 6', category: 'detail' }

            ],
            currentCategory: 'all',
            showModal: false,
            currentIndex: 0,

        };
    },mounted () {
      window.addEventListener('scroll', this.handleScroll);
    },
    methods: {

        filterImages(category) {
            this.currentCategory = category;
        },
        showImage(category) {
            return this.currentCategory === 'all' || category === this.currentCategory;
        },
        openModal(index) {
            this.showModal = true;
            this.currentIndex = index;
        },
        closeModal() {
            this.showModal = false;
        },
        plusDivs(n) {
            this.currentIndex += n;
            if (this.currentIndex >= this.images.length) {
                this.currentIndex = 0;
            }
            if (this.currentIndex < 0) {
                this.currentIndex = this.images.length - 1;
            }
        },
        currentDiv(n) {
            this.currentIndex = n;
        },
    },
    created() {
        this.filterImages('all');
    }
};
</script>



<style scoped>

#portfolio{
background-color: #2b2d33;
background-image: url("@/assets/images/macchia_viola_2.png");
    background-repeat: no-repeat;
    background-position-x: 1150px;
    background-position-y: 900px;
position: relative;
}


.yellow_brush{
    position: absolute;
    width: 135px;
    top: -2%;
    left: 3%;
}


/* SEZIONE TESTO */




span,
h3,
li{
    font-family: 'Jost',sans-serif;
    font-weight: 500;
}


span{
    color: #f75023;
    font-size: 22px;
}

h3{
    color: white;
    font-size: 38px;
    padding: 5px;
}


p{
    font-family: 'Open Sans', sans-serif;
    color: #b0acc0;
    padding-bottom: 60px;
    line-height: 2;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    color: white;
    display: inline; 
    margin-right: 30px; 
    transition: all .2s ease;
}

li:hover{
    color: #f75023;
    transition: all .3s ease;
}


/* GALLERY */

.grid-container {
    display: grid;
    grid-auto-flow: dense;
    gap: 25px;
    grid-template-columns: repeat(minmax(100px, 1fr));
    justify-content: center;
    align-content: center;
    grid-template-areas:
        "image-0 image-1 image-4"
        "image-0 image-3 image-4 "
        "image-2 image-3 image-5";
    height: 792px;
    padding-left: 100px;
    padding-right: 100px;
}

.grid-container img {
    max-width: 100%;
    position: relative;
    overflow: hidden;
    border-radius: 13px;
    transition: transform 0.5s ease;
}




.image-container:hover img {
    transform: scale(1.2);
    transition: transform 0.5s ease;

}


.image-container {
    position: relative;
    overflow: hidden;
    display: block;
    border-radius: 12px;
}



.image-0 {
    grid-area: image-0;


}

.image-0 img {
    height: 472px;
}


.image-1 {
    grid-area: image-1;
}

.image-2 {
    grid-area: image-4;
}

.image-2 img {
    height: 472px;
}

.image-3 {
    grid-area: image-2;
}

.image-3 img {
    height: 260px;
}


.image-4 {
    grid-area: image-3;
}


.image-4 img{
    height: 492px;
}


.image-5 {
    grid-area: image-5;
}

.image-5 img {
    height: 260px;   
   
}

/* modali */

.modal-header {
    border-bottom: none;

}

.modal {
    background: rgba(0, 0, 0, 0.721);
    z-index: 9994;
    top: 0;
    left: 0;
    width: 100%;
    height:100%;
    display: flex;
    visibility: visible;
   
}



.modal::-webkit-scrollbar {
    display: none;

}


.modal-dialog {
    max-width: 100%;
    max-height:100% ;
 

}

.modal-content {
    background-color: transparent;
    border: none;
    position: relative;
    width: 800px;
  height: 300px;
}




.image-fluid{
  padding-top: 30px;
    width: 100%;
    margin: 0 auto;
    display: block;
}


.image-fluid img {
    object-fit: none;
    border-radius: 0%;
    height: 70%;
    width: auto;
    position: relative;

}

.modal-body {
   width: 100%;
    overflow: hidden;
    align-items: center;
}


.fa-caret-left{
    position: absolute;
    top:80%;
    left: -40%;

}




.fa-caret-right{
    position: absolute;
    top:80%;
    right: -40%;
}



.fa-caret-left,
.fa-caret-right{
  font-size: 60px;
  background-size: 80px;
}




.btn-x {
    position: absolute;
    top: 2%;
    left: 100%;
    font-size: 20px;
    color: white;
    background: transparent;
    border-radius: 50%;
    width: 70px;
    height: 60px;
    border: none;
    
}

.btn-x:hover{
    color: white;
    border: none;
}


</style>