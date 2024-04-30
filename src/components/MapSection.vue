<template>
    <section class="map">
        <div class="map-conteiner">
            <div class="google-map"><iframe width="1100" height="375" style="border-radius:12px" id="gmap_canvas"
                    src="https://maps.google.com/maps?q=2880%20Broadway,%20New%20York&t=&z=13&ie=UTF8&iwloc=&output=embed"
                    frameborder="0" scrolling="no" marginheight="0" marginwidth="0"></iframe>
                    <a href="https://123movies-a.com"></a>
            </div>

        </div>

    </section>

</template>


<script>


export default {
    name: "MapSection",
}

</script>

<style scoped>

.map{
    background-color:#2b2d33;
}



.map-conteinerr {
    position: relative;
    text-align: center;

}

.google-map {
    overflow: hidden;
    background: none;
    padding-bottom: 200px;

}
</style>