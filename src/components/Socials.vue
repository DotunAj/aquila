<template>
  <aside>
    <ul>
      <li><a href="#"><i class="fab fa-instagram"></i></a></li>
      <li><a href="#"><i class="fab fa-twitter-square"></i></a></li>
      <li><a href="#"><i class="fab fa-snapchat-square"></i></a></li>
      <li><a href="#"><i class="fas fa-envelope-square"></i></a></li>       
    </ul>
  </aside>
</template>

<script>
export default {
    name: 'socials'
}
</script>

<style scoped>
aside{
  position: absolute;
  right: 20px;
  height: 100%;
  display: flex;
  align-items: center;
}

ul{
  list-style: none;
}

li{
  padding-bottom: 35px;
}

i{
  color: white;
  font-size: 40px ;
  transition-duration: 0.5s;
}

@media only screen and (max-width: 500px) {
  aside{
    display: none;
  }
}

</style>