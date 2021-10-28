<template>
  <div>
    <h1>bing chilling</h1>
    <a href="https://cdn.discordapp.com/attachments/707551577740804136/903394526511657000/maxresdefault.png">bing chilling</a>
    <p>
      there is a screwdriver in my asshole
    </p>
    <p v-if="rendering === 'server'">
      please send help
    </p>
    <p v-if="rendering === 'client'">Navigation is done on client side.</p>
    <ul>
      <li>oh no</li>
      <li>i am going to die</li>
    </ul>

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
