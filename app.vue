<template>
  <div class="root" @mousemove="move()">
    <div id="tracer" class="tracer-wrapper">
      <div class="tracer"></div>
    </div>
    <Header />
    <Main />
  </div>
</template>

<script>
export default {
  mounted() {},
  methods: {
    move() {
      let tracer = document.getElementById("tracer");
      let {clientX, clientY} = window.event;
      
      tracer.animate({
        left: `${clientX}px`,
        top: `${clientY}px`,
      },{duration:2000, fill:"forwards"});

    }
  }
}
</script>