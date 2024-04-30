<template>
    <div
      class="custom-cursor"
      ref="cursor"
      :class="{ active: isActive, 'link-hover': isLinkHover }"
      :style="{ top: mouseY + 'px', left: mouseX + 'px' }"
    >
      <div class="circle"></div> <!-- Il cerchio -->
      <div class="dot"></div> <!-- Il punto -->
    </div>
  </template>



<script>
export default {
  name: 'CustomCursor',
  data() {
    return {
      isActive: false,
      isLinkHover: false,
      mouseX: 0,
      mouseY: 0
    };
  },
  mounted() {
    document.addEventListener('mousemove', this.handleMouseMove);
    const links = document.querySelectorAll('a');
    links.forEach(link => {
      link.addEventListener('mouseenter', this.handleLinkEnter);
      link.addEventListener('mouseleave', this.handleLinkLeave);
    });
  },
  beforeUnmount() {
    document.removeEventListener('mousemove', this.handleMouseMove);
    const links = document.querySelectorAll('a');
    links.forEach(link => {
      link.removeEventListener('mouseenter', this.handleLinkEnter);
      link.removeEventListener('mouseleave', this.handleLinkLeave);
    });
  },
  methods: {
    handleMouseMove(event) {
      const cursor = this.$refs.cursor;
      const circle = cursor.querySelector('.circle');
      const dot = cursor.querySelector('.dot');
      const cursorSize = 40; // Dimensione del cursore
      const circleSize = 40; // Dimensione del cerchio
      const dotSize = 8; // Dimensione del punto


      // Calcola la posizione del cursore
      this.mouseX = event.clientX - cursorSize / 2;
      this.mouseY = event.clientY - cursorSize / 2;

      // Posiziona il cerchio al centro del cursore
      circle.style.top = `${cursorSize / 2 - circleSize / 2}px`;
      circle.style.left = `${cursorSize / 2 - circleSize / 2}px`;

      // Posiziona il punto al centro del cerchio
      dot.style.top = `${circleSize / 2 - dotSize / 2}px`;
      dot.style.left = `${circleSize / 2 - dotSize / 2}px`;

    },
    handleLinkEnter() {
      this.isLinkHover = true;
    },
    handleLinkLeave() {
      this.isLinkHover = false;
    }
  }
};
</script>

<style scoped>
.custom-cursor {
  position: fixed;
  z-index: 9999;
  width: 40px; /* Dimensione del cursore */
  height: 40px; /* Dimensione del cursore */
  pointer-events: none;
  transition: transform 0.2s ease;
}




.circle {
  position: absolute;
  width: 38px; 
  height: 39px; 
  border-radius: 50%;
  border: 2px solid #f75023;
}

.dot {
  position: absolute;
  width: 8px; 
  height: 8px; 
  border-radius: 50%;
  background-color: #f75023;
}


.link-hover .circle {
  display: none; 
  z-index: 9999;
}

.link-hover .dot {
  display: none;
}

.link-hover {
  position: absolute;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background-color: #d4461f59; 
  transform: scale(1.4);
    transition: transform 0.3s ease;
}












</style>