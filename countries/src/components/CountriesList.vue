<script setup>
import { useRoute } from 'vue-router';
const route = useRoute();

const countries = [
{ name: "Spain", alpha3Code: "ESP" },
{ name: "France", alphaCode: "FRA" }, 
{ name: "Germany", alphascode: "DEU" }, 
{ name: "Italy", alpha3Code: "ITA" }, 
{ name: "United Kingdom", alphacode: "GBR" }, 
{ name: "Netherlands", alpha3Code: "NLD" },
{ name: "Belgium", alpha3Code: "BEL" },
];
</script>

<template> 
<ul> 
    <li v-for= "country in countries" :key="country.alpha3Code">
    <router-link :to="'/list/${country.alpha3Code}'">{{ country.name }}</router-link>
</li>
</ul>
</template>
<style scoped>
</style>