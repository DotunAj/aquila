<template>
  <div class="menu" :class="{open_menu: menuOpened}">
    <div class="header">
      <span class="header-image">
        <img src="../assets/avatar.png" alt="avatar">
      </span>
      <div class="header-line"></div>
    </div>

    <ul class="body">
      <li><a class="active" href="#">HOME</a></li>
      <li><a href="#">ABOUT</a></li>
      <li><a href="#">GALLERY</a></li>
      <li><a href="#">CONTACT</a></li>
    </ul>

     <ul class="footer">
      <li><a href="#"><i class="fab fa-instagram"></i></a></li>
      <li><a href="#"><i class="fab fa-twitter-square"></i></a></li>
      <li><a href="#"><i class="fab fa-snapchat-square"></i></a></li>
      <li><a href="#"><i class="fas fa-envelope-square"></i></a></li>       
    </ul>
  </div>
</template>

<script>
export default {
  props: ['menuOpened']
}
</script>

<style>
.menu {
  background-color: rgba(59, 7, 26, 0.98);
  position: fixed;
  top: 0;
  right: 0;
  height: 100%;
  width: 100%;
  transition: transform 0.3s ease-in-out;
  z-index: 11;
  transform: translateX(100%);
  display: flex;
  color: #fff;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

 .header {
  margin-bottom: 20px;
  text-transform: uppercase;
  letter-spacing: 0.4em;
  position: relative;
  width: 60%;
  top: 1px;
  text-align: center;
}

.header-image img{
  padding: 0 10px;
  font-size: 16px;
  z-index: 1;
  position: relative;
  background-color: rgba(59, 7, 26, 0.98);
  height: 80px;
}

.open_menu {
  transform: translateX(0);
}

.body {
  display: flex;
  flex-direction: column;
  list-style-type: none;
  align-items: center;
  justify-content: center;
  font-size: 20px;
  padding: 0;
  margin: 0;
  font-weight: 500;
}

.body li a {
  text-decoration: none;
  cursor: pointer;
  display: inline-block;
  padding: 15px 20px;
  transition: ease-in 0.25s;
  color: #fff;
}

.body li a:hover {
  background-color: #fff;
  color: rgb(31, 29, 29) !important;
}

.body li a.active {
  background-color: #fff;
  color: rgb(31, 29, 29) !important;
}

.footer{
  list-style-type: none;
  display: flex;
  justify-content: space-between;
  margin-top: 30px;
}

.footer li{
  padding-right: 40px;
}

.footer li:last-child{
  padding-right: 0;
}

.footer i{
  color: white;
  font-size: 30px ;
  transition-duration: 0.5s;
}

</style>