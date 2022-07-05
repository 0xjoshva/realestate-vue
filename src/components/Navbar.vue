<template>
    <div class="navbar">
    <router-link to="/"><img src="https://github.com/0xjoshva/RealEstate-Website/blob/main/assets/sterlinglogoonly.png?raw=true" alt="" id="logo"></router-link>
    <router-link to="/">HOME</router-link>
    <router-link to="/property">PROPERTY</router-link>
    <router-link to="/contact">CONTACT</router-link>
    <router-link to="/admin" class="btn-listing">MANAGE LISTINGS</router-link>
  </div>
</template>
<script>
export default {
    
}
</script>
<style>
.btn-listing {
  background-color: rgba(255, 254, 254, 0.132);
  border: none;
  color: white;
  padding: 11px 15px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 12px;
  font-weight: bold;
  cursor: pointer;
  -webkit-transition-duration: 0.4s;
  transition-duration: 0.4s;
  border: 1px solid white;
  border-radius: 5px 5px;
  white-space: nowrap;
}

.btn-listing:hover{
  background-color: rgba(255, 254, 254, 0.733);
  color: #000;
}
</style>