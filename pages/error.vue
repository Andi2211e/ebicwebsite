<template>
  <div>
    <h1 v-if="error.statusCode === 404">this page doesnt exist idiot</h1>
    <h1 v-else>you fucking retard look what you did! ERROR:{{ error.statusCode }} </h1>
  </div>
</template>

<script>
  export default {
    props: ['error'],
    layout: 'error'
  }
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');
h1 {
  font-family: 'Open Sans', sans-serif;
}
p {
  font-family: 'Open Sans', sans-serif;
}
li {
  font-family: 'Open Sans', sans-serif;
</style>
