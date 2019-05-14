<template>
  <div class="app">

  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "app",
  data: () => ({}),
  async created() {
    const jsonArray = await axios
      .get(
        "https://cors-anywhere.herokuapp.com/https://www.dropbox.com/sh/04nb6vkzf68hg6o/AAB5NWERzvScgupUPmKMzRM5a?dl=0/emission.csv"
      )
      .then(result => result.data);
    console.log(jsonArray);
  }
};

</script>

<style>

</style>
