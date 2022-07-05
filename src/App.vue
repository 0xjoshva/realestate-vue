<template>
  <navbar/>
  <router-view/>
</template>
<script>
import Navbar from "./components/Navbar.vue";


export default {
  components: {
    Navbar,
  },
};
  </script>
<style>
.navbar {
  background: #3a3c3d;
  margin: 0%;
  display: flex;
  justify-content: flex-end;
  border-bottom: solid 1px white;
}

.navbar a {
  font-weight: bold;
  color: #ffffff;
  margin: 10px;
  text-decoration: none;
  font-size: 12px;
}

.navbar a.router-link-exact-active {
  color: #acacac;
}
    
#logo {
  width: auto;
  height: 50px;
  margin-bottom: 10%;
  margin: 0;
    padding: 0;
    border: 0;
    white-space: nowrap;
  
}
#home{
  background: rgb(29, 185, 84);
  background: linear-gradient(
      0deg,
      rgba(65, 67, 69, 0.6589986336331408) 0%,
      rgba(35, 37, 38, 0.8802871490393032) 100%
    ),
    url(./assets/skyline.jpg) no-repeat top center;
  background-size: cover;
  height: 87.4vh;
  width: 100%;
  margin: 0 auto;
}

</style>


