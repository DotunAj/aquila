<template>
  <nav>
    <ul>
      <li>
        <a href="#">HOME</a>
      </li>
      <li>
        <a href="#">ABOUT</a>
      </li>

      <li class="avatar">
        <img src="../assets/avatar.png" alt="avatar">
      </li>

      <li>
        <a href="#">GALLERY</a>
      </li>
      <li>
        <a href="#">CONTACT</a>
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'navigation'
}
</script>

<style scoped>
ul{
  display: flex;
  list-style: none;
  justify-content: center;
  align-items: center;
}
li{
  padding-right: 30px;
}

li:first-child{
  margin-right: 90px;
}

li:last-child{
  padding-right: 0;
}

a{
  text-decoration: none;
  font-weight: 300;
  font-size: 16px;
    letter-spacing: 12px;
  color: white;
}

@media only screen and (max-width: 850px) {
  a{
    font-size: 13px;
    letter-spacing: 12px;
    color: white;
  }

  li{
    padding-right: 20px;
  }

  img{
    width: 80px;
  }

  li:first-child{
    margin-right: 60px;
  }

  ul{
    display: flex;
    list-style: none;
    justify-content: center;
    align-items: center;
  }
}

@media only screen and (max-width: 500px) {
  nav{
    display: none;
  }
}
</style>