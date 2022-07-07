<template>
  <div class="card">
    <div class="box">
      <figure>
        <router-link :to="{ name:'PropertyDetails', params:{id: property.id} }">
        <img v-bind:src="property.imageURL" alt="" class="house-image" />
        </router-link>
        <figcaption>
          $<span>{{ property.price }}</span
          >/mo
        </figcaption>
      </figure>
      <div id="text">
        <h3 class="pt-1" id="title">{{ property.title }}</h3>
        <p class="lead text-muted" id="address">
          <i class="bi bi-geo"></i> {{ property.address }}
        </p>
        <div class="icons">
          <div>
            <i class="fa-solid fa-bed"></i
            ><span id="bedrooms"> {{ property.bedrooms }}</span>
          </div>
          <div>
            <i class="fa-solid fa-shower"></i
            ><span id="bathrooms"> {{ property.bathrooms }}</span>
          </div>
          <div>
            <i class="fa-solid fa-warehouse"></i
            ><span id="garages"> {{ property.garages }}</span>
          </div>
          <div>
            <i class="fa-solid fa-ruler-combined"></i
            ><span id="size"> {{ property.size }}</span
            ><span> ㎡</span>
          </div>
        </div>
        <p id="property-type">{{ property.category }}</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["property"],
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
