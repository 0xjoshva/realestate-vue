<template>
  <div class="card">
    <div class="box">
      <figure>
        <img v-bind:src="property.imageURL" alt="" class="house-image" />
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
<style></style>
