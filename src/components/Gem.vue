<template>
    <div>
        <p>content changed {{imageSource}} </p>
        <p> {{generatedImageSource}} </p>
        <!-- <img src="assets/crystal1.png"> -->
        <img alt="regular htmls" src="../assets/crystal1.png">
        <img alt="using data val" v-bind:src="image">
        <img alt="computed val" :src= "generatedImageSource">
    </div>
</template>

<script>
export default {
    name:'Gem',
    data: function() {
        return{
            image: "../assets/crystal1.png"
        }
        
    },
    props:{
        imageSource: String,
        // image: '../assets/crystal1.png'
    },
    computed:{
        generatedImageSource: function(){
            const relativeSource = "../assets/crystal";
            return relativeSource + this.imageSource + ".png";
            }
        
    }
}
</script>

<style scoped>
p{
    color: #fefefe;
}
</style>