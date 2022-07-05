<template>
  <div id="home">
   <h1 class="text-center" id="heading">STERLING PROPERTY ADVISORS</h1>
      <p id="subheading">
        At Sterling Real Estate, you are number one. Whether you are a property
        owner, tenant, or buyer, we value your business and will provide you
        with the individual attention and service you deserve. We believe in a
        strict Code of Ethics.
      </p>
      </div>
</template>

<style>


#heading {
  font-family: "Open Sans", sans-serif !important;
  font-weight: 900;
  letter-spacing: 2px;
  padding-top: 8%;
  color: white;
  z-index: 1;
  -webkit-mask-image: linear-gradient(
    -75deg,
    rgba(0, 0, 0, 0.6) 30%,
    #000 50%,
    rgba(0, 0, 0, 0.6) 70%
  );
  -webkit-mask-size: 200%;
  animation: shine 2s linear infinite;
}

@keyframes shine {
  from {
    -webkit-mask-position: 150%;
  }
  to {
    -webkit-mask-position: -50%;
  }
}
#subheading {
  margin: auto;
  width: 30%;
  text-align: center;
  font-size: 18px;
  font-family: "Roboto", sans-serif;
  color: rgba(181, 181, 181, 0.8);
}
</style>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
