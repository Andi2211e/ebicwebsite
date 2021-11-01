<template>
  <div>
    <a href="/tacdrip.png">drip</a>
    <img src="~/static/tacdrip.png" />
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
