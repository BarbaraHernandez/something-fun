<template>
  <div>
    <p>content changed {{imageSource}}</p>
    <p>{{generatedImageSource}}</p>
    <!-- <img src="assets/crystal1.png"> -->
    <img alt="regular htmls" src="../assets/crystal1.png" />
    <img alt="using data val" :src="image" />
    <img alt="computed val" :src="generatedImageSource" />
  </div>
</template>

<script>
export default {
  // require is necessary to resolve the webpack generated name
  // for the image. Require does not allow one to use an expression
  // so don't bother using es6 features.s
  name: "Gem",
  data: function() {
    return {
      image: require("../assets/crystal1.png")
    };
  },
  props: {
    imageSource: String
  },
  computed: {
    generatedImageSource: function() {
      return require("../assets/crystal" + this.imageSource + ".png");
    }
  }
};
</script>

<style scoped>
p {
  color: #fefefe;
}
</style>