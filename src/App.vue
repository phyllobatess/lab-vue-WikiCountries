<script setup>

import {onMounted} from "vue";
import NavBar from "./components/NavBar.vue"
import CountriesList from './components/CountriesList.vue'
import CountryDetails from './components/CountryDetails.vue'

</script>

<template> 
<div class="app">
    <NavBar/>
    <RouterView/>
</div>
</template>


