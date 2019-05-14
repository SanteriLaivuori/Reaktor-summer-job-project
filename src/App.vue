<template>
  <div class="app">

  </div>
</template>

<script>
// import emission from "@/assets/emission.csv";
import axios from "axios";

export default {
  name: "app",
  data: () => ({}),
  async created() {
    const jsonArray = await axios
      .get(
        "https://cors-anywhere.herokuapp.com/http://snowcoding.com/reaktor/emission.csv"
      )
      .then(result => result.data);
    console.log(jsonArray);
  }
};
</script>

<style>
.app {
  background-image: url("https://fw-d7-freedomworks-org.s3.amazonaws.com/field/image/70250513-factory-wallpapers.jpg");
  background-position: center;
  background-size: cover;

}
</style>
