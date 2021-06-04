<template>
  <div
    class="slide"
    :style="{ backgroundImage: 'url(' + slide.images[0] + ')' }"
  >
    <span class="spacer"></span>
    <transition name="slide-right" appear>
      <h1>{{ slide.title }}</h1>
    </transition>
    <transition name="slide-left" appear>
      <p>{{ slide.description }}</p>
    </transition>
    <transition name="slide-up" appear>
      <button class="btn" @click="getInTouch()">GET IN TOUCH</button>
    </transition>
    <span class="spacer"></span>
  </div>
</template>
<script>
export default {
    name: 'Slide',
    methods: {
        getInTouch() {
            this.$emit('getInTouch');
        }
    },
    props: ['slide']
};
</script>
