<template>
  <div class="loader-container">
    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" style="margin: auto; background: rgba(255, 255, 255, 0); display: block; shape-rendering: auto;" width="200px" height="200px" viewBox="0 0 100 100" preserveAspectRatio="xMidYMid">
    <circle cx="50" cy="50" fill="none" stroke="#ffffff" stroke-width="5" r="25" stroke-dasharray="117.80972450961724 41.269908169872416">
      <animateTransform attributeName="transform" type="rotate" repeatCount="indefinite" dur="2.8571428571428568s" values="0 50 50;360 50 50" keyTimes="0;1"></animateTransform>
    </circle>
    <!-- [ldio] generated by https://loading.io/ --></svg>
  </div>
</template>


<style  scoped>
.loader-container {
  background-color: rgba(59, 7, 26, 0.98);
  z-index: 1001;
  position: fixed;
  top: 0;
  min-height: 200px;
  height: 100vh;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

svg {
  fill: #868686;

}
  path:nth-of-type(1) {
    animation: pulse 1s infinite linear;
  }
  path:nth-of-type(2) {
    animation: pulse 1s -0.083s infinite linear;
  }
  path:nth-of-type(3) {
    animation: pulse 1s -0.166s infinite linear;
  }
  path:nth-of-type(4) {
    animation: pulse 1s -0.249s infinite linear;
  }
  path:nth-of-type(5) {
    animation: pulse 1s -0.332s infinite linear;
  }
  path:nth-of-type(6) {
    animation: pulse 1s -0.415s infinite linear;
  }
  path:nth-of-type(7) {
    animation: pulse 1s -0.498s infinite linear;
  }
  path:nth-of-type(8) {
    animation: pulse 1s -0.581s infinite linear;
  }
  path:nth-of-type(9) {
    animation: pulse 1s -0.664s infinite linear;
  }
  path:nth-of-type(10) {
    animation: pulse 1s -0.747s infinite linear;
  }
  path:nth-of-type(11) {
    animation: pulse 1s -0.83s infinite linear;
  }
  path:nth-of-type(12) {
    animation: pulse 1s -0.913s infinite linear;
  }

@keyframes pulse {
  50% {
    fill: #868686;
  }
  to {
    fill: rgba(134, 134, 134, 0.4);
  }
}
</style>
