<template>
  <div class="home">
    <nav-bar></nav-bar>
    <slides></slides>
  </div>
</template>

<script>
import NavBar from '@/components/NavBar';
import Slides from '@/components/Slides';
export default {
  name: 'Home',
  components: {
    NavBar,
    Slides
  }
}
</script>
