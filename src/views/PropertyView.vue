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

</style>
