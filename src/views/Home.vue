<template>
  <div class="header">
    <div class="header__search">
      <div class="search__container">
        <h1>IP Address Tracker</h1>
        <div class="search__input">
          <input
            type="text"
            placeholder="Search for any IP address or leave empty to get your ip info"
          />
          <i class="fas fa-chevron-right chevron"></i>
        </div>
        <IPInfo />
      </div>
      <div id="map" class="map"></div>
    </div>
  </div>
</template>

<script>
import IPInfo from "@/components/IPInfo";
import { onMounted } from "vue";
import leaflet from "leaflet";

export default {
  name: "Home",
  components: { IPInfo },
  setup() {
    let myMap;
    onMounted(() => {
      myMap = leaflet.map("map").setView([51.505, -0.09], 13);

      leaflet
        .tileLayer(
          "https://api.mapbox.com/styles/v1/{id}/tiles/{z}/{x}/{y}?access_token=pk.eyJ1IjoiYW5keWJlYWJsZSIsImEiOiJja2tvNHFsbzcwemdzMm9uc3d3cmNudjB4In0.YRvihj2bTJkl4z1zTpbByw",
          {
            attribution:
              'Map data &copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors, Imagery © <a href="https://www.mapbox.com/">Mapbox</a>',
            maxZoom: 18,
            id: "mapbox/streets-v11",
            tileSize: 512,
            zoomOffset: -1,
            accessToken:
              "pk.eyJ1IjoiYW5keWJlYWJsZSIsImEiOiJja2tvNHFsbzcwemdzMm9uc3d3cmNudjB4In0.YRvihj2bTJkl4z1zTpbByw",
          }
        )
        .addTo(myMap);
    });
  },
};
</script>

<style lang="scss">
.header {
  display: flex;
  flex-direction: column;
  height: 245px;
  background-image: url("~@/assets/pattern-bg.png");
  background-size: cover;
  background-repeat: no-repeat;
  padding-top: 10px;

  h1 {
    color: #fff;
    text-align: center;
    font-size: 29px;
    font-weight: 500;
  }
}

.search__container {
  margin: 1rem 2rem;
}

.search__input {
  display: flex;
  justify-content: center;
  position: relative;
  max-width: 500px;
  margin: 1.5rem auto;
}

input {
  width: 100%;
  padding: 28px 0px 28px 21px;
  border: none;
  border-top-left-radius: 16px;
  border-bottom-left-radius: 16px;
  height: 30px;
}
input:focus {
  outline: none;
}

input::placeholder {
  font-size: 16px;
  color: #b0afaf;
}

.chevron {
  cursor: pointer;
  background: #000;
  color: #fff;
  padding: 20.5px;
  border-top-right-radius: 16px;
  border-bottom-right-radius: 16px;
  display: flex;
  align-items: center;
}

.map {
  height: 100%;
  z-index: 10;
}
</style>
