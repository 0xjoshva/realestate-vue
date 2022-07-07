<template>
  <div v-if="property" id="propertydetails">
  <div id="container-12">
  <div class="heading-details pt-5 py-3">
  <div>
    <h1>{{ property.title }}</h1>
    <h6 class="text-muted lead address-details"><i class="bi bi-geo"></i>{{property.address}}</h6></div>

    <div id="price-size">
        <h2>${{property.price}}</h2>
        <h5 class="text-muted lead size-details">{{property.size}} Sq Ft</h5>
    </div>
    </div>
    </div>
    <div class="image-containe">
    <img v-bind:src="property.imageURL" alt="" class="imageURL"/></div>
    <router-view/>

<div class="overview-container">
    <div class="overview">
        <div id="section1-container">
        <div id="section-1">
        <h1 id="overview-head">Overview</h1>
        <h3 class="fw-bold" id="propID-text"> Property ID: <span class="fw-lighter">{{ id }}</span></h3>
        </div></div>
<div class="hrdiv">
   <hr/></div>
        <div id="info-container1">
          <div class="info">
        <span class="fw-bold"> {{ property.category }} </span>
        <span class="info-info">Property Type</span>
          </div>
          <div class="info">
        <span class="fw-bold"> <i class="fa-solid fa-bed"></i> {{ property.bedrooms }} </span>
        <span class="info-info">Bedrooms</span>
          </div>
          <div class="info">
        <span class="fw-bold"><i class="fa-solid fa-shower"></i> {{ property.bathrooms }} </span>
        <span class="info-info">Bathrooms</span>
          </div>
          <div class="info">
        <span class="fw-bold"> <i class="fa-solid fa-warehouse"></i> {{ property.garages }} </span>
        <span class="info-info">Garage</span>
          </div>
          <div class="info">
        <span class="fw-bold"> {{ property.size }} </span>
        <span class="info-info">Sq Ft</span>
          </div>


        </div>
</div></div>
    </div>
</template>
<script>
export default {
    props: ["id"],
       data() {
            return {
                property: null,
            };
        },
        mounted() {
            fetch("http://localhost:3000/properties/" + this.$route.params.id)
                .then((res) => res.json())
                .then((data) => (this.property = data))
        },

 
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;500;600;700;800&family=Roboto:wght@100;300;400;500;700;900&display=swap");
.heading-details{
    width: 1000px;
    display:flex;
    justify-content: space-between;
    flex-direction: row;
}
#container-12{
    display: flex;
    justify-content: center;
}
.imageURL{
    border-radius: 5px 5px;
    width: 1000px;
    height: 550px

}
.image-containe{
    display: flex;
    justify-content: center;
}
.address-details{
    font-family: "Roboto", sans-serif;
    font-size: 15px;
}
.size-details{
    font-family: "Roboto", sans-serif;
    font-size: 18px;
}
#price-size{
    text-align: end;
}
#propertydetails{
background: rgb(244, 244, 244);}

.overview-container{
    padding-bottom: 3%;
    padding-top: 3%;
    display: flex;
    justify-content: center;
    font-family: "Roboto", sans-serif;
}
.overview{
    padding: 20px;
    width: 1000px;
background: white;
border-radius: 5px 5px;
}
#section-1{
    display: flex;
    flex-direction:row;
    justify-content: space-between;
    width: 850px;
    
}
.info{
    display: flex;
    flex-direction: column;
}
hr{
    width: 90%;
}
#info-container1{
    display: flex;
    flex-direction:row;
    justify-content: space-around;
}
.hrdiv{
    display:flex;
    justify-content: center;
}
#propID-text{
font-size: 16px;
}
#overview-head{
    font-size: 18px;
}
#info-info{
    font-weight: 300;
    font-family: "Roboto", sans-serif;
    line-height:25px;
}
#section1-container{
    display: flex;
    justify-content: center;
}
</style>
