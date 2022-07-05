<template>
  <h1 class="text-center" id="heading-2">Discover Our Featured Listings</h1>
  <p class="text-center text-muted" id="subheading-2">
    browse trending houses/apartments
  </p>

  <div id="box-container">
    
    <!-- card here -->
    <PropertyCard
      v-for="property in properties"
      :key="property.id"
      :property="property"
      class="property"
    />

  </div>
</template>
<script>
import PropertyCard from "@/components/PropertyCard.vue";
export default {
  components: { PropertyCard },
  data() {
    return {
      properties: [],
    };
  },
  mounted() {
    fetch("http://localhost:3000/properties")
      .then((res) => res.json())
      .then((data) => {
        console.log(data)
        this.properties = data
      })
      .catch((err) => console.log(err.message));
  },
  components: { PropertyCard },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;500;600;700;800&family=Roboto:wght@100;300;400;500;700;900&display=swap");

.box {
  height: max-content;
  width: max-content;
  background: transparent;
  flex-basis: 33.333333%;
  border-radius: 4px 4px;
  transition: all 0.7s ease-in-out;
}

#box-container {
  padding-left: 0;
  display: flex;
  flex-wrap: wrap;
  height: fit-content;
  row-gap: 20px;
  column-gap: 20px;
  justify-content: center;
  padding-bottom: 10%;
  /* flex-basis: 33.333333%; */
}

.house-image:hover {
  filter: brightness(110%);

  /* transform: translateY(-3px); */
}
.box:hover {
  transform: translateY(-5px);
}

figure {
  position: relative;
}
figcaption {
  font-size: 20px;
  position: absolute;
  width: fit-content;
  text-align: center;
  left: 15px;
  top: 260px;
  color: white;
  font-weight: 500;
  font-family: "Roboto", sans-serif;
}

.house-image {
  height: 300px;
  /* box-shadow: 0px 0px 40px 0px rgb(0 0 0 / 30%); */
  width: 400px;
  border-radius: 4px 4px 0px 0px;
  filter: brightness(70%);
  transition: all 1s ease-in-out;
}

#discover {
  background: rgb(255, 255, 255);
  background: linear-gradient(
    0deg,
    rgba(255, 255, 255, 1) 0%,
    rgba(238, 238, 238, 1) 100%
  );
}

input[type="email"]::placeholder {
  padding: 10px !important;
}

#title {
  margin-top: 2%;
  font-family: "Open Sans", sans-serif;
  font-size: larger;
  margin: 0 auto;
}
#address {
  padding-top: 2px;
  font-family: "Roboto", sans-serif;
  margin: 0 auto;
  font-size: 14px;
}
#bedrooms {
  font-family: "Roboto", sans-serif;
}
#bathrooms {
  font-family: "Roboto", sans-serif;
}
#garages {
  font-family: "Roboto", sans-serif;
}
#size {
  font-family: "Roboto", sans-serif;
}
#property-type {
  font-family: "Open Sans", sans-serif;
  font-size: 13px;
  font-weight: 600;
}

.icons {
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  column-gap: 16px;
  font-weight: 300;
  font-size: 13px;
  padding-top: 10px;
  padding-bottom: 3px;
}

#text {
  margin-left: 1%;
}

#heading-2 {
  padding-top: 7%;
  font-smooth: 20em;
  font-size: 40px;
  font-weight: 300;
  font-family: "Open Sans", sans-serif;
}
#subheading-2 {
  padding-bottom: 5%;
}
</style>
