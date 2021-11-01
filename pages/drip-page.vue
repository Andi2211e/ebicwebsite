<template>
  <div>
    <h1 href="/tacdrip.png">drip</h1>
    <img src="~/static/bingchilling.png" />

    <NuxtLink to="/about">this goes nowhere</NuxtLink>
  </div>
</template>
<script>
export default {
  asyncData() {
    return {
      rendering: process.server ? 'server' : 'client'
    }
  }
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
}
NuxtLink {
  font-family: 'Open Sans', sans-serif;
}
</style>
