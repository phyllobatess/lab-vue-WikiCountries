<template>
    <h1>Hellooo</h1>
</template>

<script setup>
//data properties
const countries = ref(null);

//methods/functions
const fetchCountries = async () => {
  const response = await fetch(
    "https://ih-countries-api.herokuapp.com/countries"
  );

  const finalResponse = await response.json();

  const sortedCountries = finalResponse.sort((a, b) => {
    return a.name.common.localeCompare(b.name.common);
  });

  countries.value = sortedCountries;
};

fetchCountries();
</script>

<style scopped></style>